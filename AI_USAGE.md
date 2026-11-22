# AI usage disclosure

## Tools used
ChatGPT was used to assist with project scaffolding, component implementation, responsive CSS, task logic, documentation, and reviewing the assignment checklist.


## Representative prompts
1. "Build a responsive React task dashboard with task creation, edit/delete, statuses, search, filters, calculated stats, a 3-slide Focus Notes carousel, and localStorage persistence."
2. "Implement accessible controls and a mobile-friendly sidebar/task form."
3. "Create documentation explaining setup, state management, deployment and known limitations."

## AI-assisted areas
- Initial React component structure and sample task data
- Task CRUD and status controls
- Derived dashboard statistics, search and combined filtering
- Focus Notes carousel state and controls
- Responsive CSS styling
- README and this disclosure


## Review / correction
The dashboard uses the task array as the single source of truth and calculates the statistics from that array rather than hardcoding values. Task updates use functional state updates and map/filter operations. The Figma design itself was not accessible from this environment, so exact colors, spacing, and Focus Notes text remain to be checked against the reference before final submission. I have not run a production build here because package installation timed out; verify with `npm install` and `npm run build` locally.


## Understanding
Before presenting or submitting, review the React state flow, derived counts, filter combination, localStorage initialization/write behavior, form validation, status mutation, and delete confirmation. Be prepared to explain and modify one small feature live.
