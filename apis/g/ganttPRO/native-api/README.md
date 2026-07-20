# GanttPRO: Native API Reference

A consolidated summary of GanttPRO's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.ganttpro.com/index.html
- **API base URL:** `https://api.ganttpro.com/v1.0`

## Authentication

### API Key

Authenticate GanttPRO API requests with the team API key in the X-API-KEY header.

### Credentials

- **GanttPRO API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://developer.ganttpro.com/index.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Resource To Task](actions/assign-resource-to-task.md) | `POST /tasks/:taskId/assignResource` | [docs](https://developer.ganttpro.com/index.html) |
| [Create Project Custom Day](actions/create-project-custom-day.md) | `POST /projects/customday` | [docs](https://developer.ganttpro.com/index.html) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developer.ganttpro.com/index.html) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /comments` | [docs](https://developer.ganttpro.com/index.html) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE /attachments/:attachmentId` | [docs](https://developer.ganttpro.com/index.html) |
| [Delete Project Custom Day](actions/delete-project-custom-day.md) | `DELETE /projects/customday/:customDayId` | [docs](https://developer.ganttpro.com/index.html) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://developer.ganttpro.com/index.html) |
| [Delete Task Comment](actions/delete-task-comment.md) | `DELETE /comments/:commentId` | [docs](https://developer.ganttpro.com/index.html) |
| [Get Current Team](actions/get-current-team.md) | `GET /team` | [docs](https://developer.ganttpro.com/index.html) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://developer.ganttpro.com/index.html) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://developer.ganttpro.com/index.html) |
| [List Project Calendars](actions/list-project-calendars.md) | `GET /projects/calendars` | [docs](https://developer.ganttpro.com/index.html) |
| [List Project Comments](actions/list-project-comments.md) | `GET /comments/getByProjectId` | [docs](https://developer.ganttpro.com/index.html) |
| [List Project Task Fields](actions/list-project-task-fields.md) | `GET /projects/taskFields` | [docs](https://developer.ganttpro.com/index.html) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developer.ganttpro.com/index.html) |
| [List Resources](actions/list-resources.md) | `GET /resources` | [docs](https://developer.ganttpro.com/index.html) |
| [List Task Comments](actions/list-task-comments.md) | `GET /comments` | [docs](https://developer.ganttpro.com/index.html) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developer.ganttpro.com/index.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developer.ganttpro.com/index.html) |
| [Remove Resource From Task](actions/remove-resource-from-task.md) | `DELETE /tasks/:taskId/assignResource` | [docs](https://developer.ganttpro.com/index.html) |
| [Update Project Custom Day](actions/update-project-custom-day.md) | `PUT /projects/customday/:customDayId` | [docs](https://developer.ganttpro.com/index.html) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://developer.ganttpro.com/index.html) |
| [Update Task Comment](actions/update-task-comment.md) | `PUT /comments/:commentId` | [docs](https://developer.ganttpro.com/index.html) |
| [Update User Notification Settings](actions/update-user-notification-settings.md) | `PUT /users/:userId/notification` | [docs](https://developer.ganttpro.com/index.html) |
