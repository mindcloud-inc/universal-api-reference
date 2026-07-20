# Nozbe Teams: Native API Reference

A consolidated summary of Nozbe Teams's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://api4.nozbe.com/v1/api
- **OpenAPI specification:** https://api4.nozbe.com/v1/api/openapi.yaml
- **API base URL:** `https://api4.nozbe.com/v1/api`

## Authentication

### API Token

Nozbe API token sent as the raw Authorization header value on every request.

### Credentials

- **API Token:** `apiToken` · required · Nozbe API token. The runtime sends this exact raw value in the Authorization header on every request.

Send these headers with each API request:

```http
Authorization: <apiToken>
```

[Official authentication documentation](https://api4.nozbe.com/v1/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `API-Version` | `128` |

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://api4.nozbe.com/v1/api#/comments/postComment) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://api4.nozbe.com/v1/api#/projects/postProject) |
| [Create Project From Template](actions/create-project-from-template.md) | `POST /projects/from_template/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/postProjectFromTemplate) |
| [Create Project Section](actions/create-project-section.md) | `POST /project_sections` | [docs](https://api4.nozbe.com/v1/api#/project_sections/postProjectSection) |
| [Create Reminder](actions/create-reminder.md) | `POST /reminders` | [docs](https://api4.nozbe.com/v1/api#/reminders/postReminder) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://api4.nozbe.com/v1/api#/tasks/postTask) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/deleteCommentById) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/deleteProjectById) |
| [Delete Project Section](actions/delete-project-section.md) | `DELETE /project_sections/:id` | [docs](https://api4.nozbe.com/v1/api#/project_sections/deleteProjectSectionById) |
| [Delete Reminder](actions/delete-reminder.md) | `DELETE /reminders/:id` | [docs](https://api4.nozbe.com/v1/api#/reminders/deleteReminderById) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/deleteTaskById) |
| [Get Comment](actions/get-comment.md) | `GET /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/getCommentById) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/getProjectById) |
| [Get Project Section](actions/get-project-section.md) | `GET /project_sections/:id` | [docs](https://api4.nozbe.com/v1/api#/project_sections/getProjectSectionById) |
| [Get Reminder](actions/get-reminder.md) | `GET /reminders/:id` | [docs](https://api4.nozbe.com/v1/api#/reminders/getReminderById) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/getTaskById) |
| [Get Task Event](actions/get-task-event.md) | `GET /task_events/:id` | [docs](https://api4.nozbe.com/v1/api#/task_events/getTaskEventById) |
| [Get Team](actions/get-team.md) | `GET /teams/:id` | [docs](https://api4.nozbe.com/v1/api#/teams/getTeamById) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://api4.nozbe.com/v1/api#/comments/getComments) |
| [List Project Sections](actions/list-project-sections.md) | `GET /project_sections` | [docs](https://api4.nozbe.com/v1/api#/project_sections/getProjectSections) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://api4.nozbe.com/v1/api#/projects/getProjects) |
| [List Reminders](actions/list-reminders.md) | `GET /reminders` | [docs](https://api4.nozbe.com/v1/api#/reminders/getReminders) |
| [List Task Events](actions/list-task-events.md) | `GET /task_events` | [docs](https://api4.nozbe.com/v1/api#/task_events/getTaskEvents) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://api4.nozbe.com/v1/api#/tasks/getTasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://api4.nozbe.com/v1/api#/teams/getTeams) |
| [Poll New Tasks](actions/poll-new-tasks.md) | `GET /poll/tasks/new` | [docs](https://api4.nozbe.com/v1/api#/other/pollTasksNew) |
| [Poll Updated Tasks](actions/poll-updated-tasks.md) | `GET /poll/tasks/updated` | [docs](https://api4.nozbe.com/v1/api#/other/pollTasksUpdated) |
| [Update Comment](actions/update-comment.md) | `PUT /comments/:id` | [docs](https://api4.nozbe.com/v1/api#/comments/putCommentById) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://api4.nozbe.com/v1/api#/projects/putProjectById) |
| [Update Project Section](actions/update-project-section.md) | `PUT /project_sections/:id` | [docs](https://api4.nozbe.com/v1/api#/project_sections/putProjectSectionById) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://api4.nozbe.com/v1/api#/tasks/putTaskById) |
