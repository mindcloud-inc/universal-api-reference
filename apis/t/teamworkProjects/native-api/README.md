# Teamwork Projects: Native API Reference

A consolidated summary of Teamwork Projects's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.teamwork.com/docs/teamwork
- **API base URL:** `{apiEndPoint}projects/api/v3`

## Authentication

### OAuth 2.0

Authenticate users with Teamwork.com's App Login Flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.teamwork.com/launchpad/login/ to approve access.
2. Exchange the returned authorization code with a POST request to https://www.teamwork.com/launchpad/v1/token.json.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://apidocs.teamwork.com/guides/teamwork/app-login-flow)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderMode`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Project Task List Report](actions/generate-project-task-list-report.md) | `GET /projects/{{projectId}}/tasklists.html` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/task-lists/get-projects-api-v3-projects-project-id-tasklists-html) |
| [Get Notebook](actions/get-notebook.md) | `GET /notebooks/{{notebookId}}.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/notebooks/get-projects-api-v3-notebooks-notebook-id-json) |
| [Get Project](actions/get-project.md) | `GET /projects/{{projectId}}.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/projects/get-projects-api-v3-projects-project-id-json) |
| [Get Task](actions/get-task.md) | `GET /tasks/{{taskId}}.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/tasks/get-projects-api-v3-tasks-task-id-json) |
| [List Comments](actions/list-comments.md) | `GET /comments.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/comments/get-projects-api-v3-comments-json) |
| [List Companies](actions/list-companies.md) | `GET /companies.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/companies/get-projects-api-v3-companies-json) |
| [List Messages](actions/list-messages.md) | `GET /messages.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/messages/get-projects-api-v3-messages-json) |
| [List Milestones](actions/list-milestones.md) | `GET /milestones.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/milestones/get-projects-api-v3-milestones-json/) |
| [List Notebook Versions](actions/list-notebook-versions.md) | `GET /notebooks/{{notebookId}}/versions.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/notebooks/get-projects-api-v3-notebooks-notebook-id-versions-json) |
| [List Notebooks](actions/list-notebooks.md) | `GET /notebooks.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/notebooks/get-projects-api-v3-notebooks-json) |
| [List People](actions/list-people.md) | `GET /people.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/people/get-projects-api-v3-people-json) |
| [List Project Risks](actions/list-project-risks.md) | `GET /projects/{{projectId}}/risks` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/risks/get-projects-api-v3-projects-project-id-risks/) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/{{projectId}}/tasks.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/tasks/get-projects-api-v3-projects-project-id-tasks-json) |
| [List Project Updates](actions/list-project-updates.md) | `GET /projects/updates.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/project-updates/get-projects-api-v3-projects-updates-json) |
| [List Projects](actions/list-projects.md) | `GET /projects.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/projects/get-projects-api-v3-projects-json) |
| [List Sample Projects](actions/list-sample-projects.md) | `GET /projects/teamwork/samples.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/projects/get-projects-api-v3-projects-teamwork-samples-json) |
| [List Skills](actions/list-skills.md) | `GET /skills.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/skills/get-projects-api-v3-skills-json) |
| [List Tags](actions/list-tags.md) | `GET /tags.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/tags/get-projects-api-v3-tags-json) |
| [List Task Comments](actions/list-task-comments.md) | `GET /tasks/{{taskId}}/comments.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/task-comments/get-projects-api-v3-tasks-task-id-comments-json) |
| [List Task Lists](actions/list-task-lists.md) | `GET /tasklists` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/task-lists/get-projects-api-v3-tasklists) |
| [List Task Time Entries](actions/list-task-time-entries.md) | `GET /tasks/{{taskId}}/time.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/time-tracking/get-projects-api-v3-tasks-task-id-time-json) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/tasks/get-projects-api-v3-tasks-json) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/time-tracking/get-projects-api-v3-time-json) |
| [List Timesheets](actions/list-timesheets.md) | `GET /timesheets.json` | [docs](https://apidocs.teamwork.com/docs/teamwork/v3/timesheets/get-projects-api-v3-timesheets-json) |
