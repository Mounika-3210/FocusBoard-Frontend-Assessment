# FocusBoard

A responsive single-user task dashboard built with React + Vite. The project is frontend-only and persists tasks in `localStorage`.


## Features
- Dashboard totals, in-progress/completed counts and completion rate are derived from the current task list.
- Seeded sample tasks (7) include unique IDs, title, description, category, status, priority and due date.
- Create and edit tasks in a form; task title is required with a helpful validation message.
- Delete tasks after browser confirmation.
- Update task status from a dropdown or mark/unmark completed from the checkbox.
- Case-insensitive title search, status tabs and priority filter combine.
- Focus Notes carousel with 3 slides, previous/next buttons and slide dots.
- Responsive sidebar navigation, dashboard, task list and form for desktop, tablet and mobile.
- Tasks restore from local storage after refresh. Existing saved state takes precedence over sample data.
- Semantic buttons, form labels, focus styles, and accessible names for icon-only controls.


## Tech stack
- React 18+ (latest compatible version)
- Vite
- JavaScript
- Lucide icons
- CSS (custom responsive styling)


## Run locally
Requires Node.js 18+ and npm.

```bash
npm install
npm run dev
```
Open the local URL shown by Vite.


## Build for production
```bash
npm run build
npm run preview
```

The production bundle is written to `dist/`.


## State management
React `useState` is the state-management approach and the task array is the single source of truth. Add/edit/delete/status operations use functional state updates and map/filter rather than mutating task objects. Counts and filtered results are derived from task state with `useMemo`. The current task list is serialized to `localStorage` under `focusboard.tasks` and read once during initial state setup, so seed data does not overwrite existing saved tasks.


## Deployment
Deploy the repository to Vercel or Netlify as a Vite app. Build command: `npm run build`; output directory: `dist`. No backend, credentials, or environment variables are needed.


## Limitations / verification notes
- The Figma file was linked in the assignment PDF but could not be opened from this environment. The UI is an original dashboard interpretation based on the written scope and supplied PDF, not a verified pixel-perfect copy of the Figma frames. Review and tune spacing, typography, content, and slide copy against the live Figma design before submission.
- The Focus Notes copy is sample copy because the exact Figma slide content was inaccessible.
- Screenshots of the actual running app should be captured at desktop and mobile widths before submission. They are not included in this archive because dependencies could not be installed in this environment to run and verify the React app.
- The assignment expects both a public GitHub repository and a hosted HTTPS URL. These are not included yet; deploy and publish after testing.
