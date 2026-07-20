# GoodDay.work: Native API Reference

A consolidated summary of GoodDay.work's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://www.goodday.work/developers/api-v2
- **API base URL:** `https://api.goodday.work/2.0`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.goodday.work/developers/api-v2/connect)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Comment On Task](actions/comment-on-task.md) | `POST /task/:taskId/comment` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://www.goodday.work/developers/api-v2/events) |
| [Create Folder](actions/create-folder.md) | `POST /projects/new-folder` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [Create Project](actions/create-project.md) | `POST /projects/new-project` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [Delete Event](actions/delete-event.md) | `DELETE /event/:eventId` | [docs](https://www.goodday.work/developers/api-v2/events) |
| [Delete Task](actions/delete-task.md) | `DELETE /task/:taskId` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [Get Document](actions/get-document.md) | `GET /document/:documentId` | [docs](https://www.goodday.work/developers/api-v2/documents) |
| [Get Event](actions/get-event.md) | `GET /event/:eventId` | [docs](https://www.goodday.work/developers/api-v2/events) |
| [Get Project](actions/get-project.md) | `GET /project/:projectId` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [Get Task](actions/get-task.md) | `GET /task/:taskId` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [Get User](actions/get-user.md) | `GET /user/:userId` | [docs](https://www.goodday.work/developers/api-v2/users) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /custom-fields` | [docs](https://www.goodday.work/developers/api-v2/custom-fields) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://www.goodday.work/developers/api-v2/events) |
| [List Offices](actions/list-offices.md) | `GET /offices` | [docs](https://www.goodday.work/developers/api-v2/system) |
| [List Project Documents](actions/list-project-documents.md) | `GET /project/:projectId/documents` | [docs](https://www.goodday.work/developers/api-v2/documents) |
| [List Project History](actions/list-project-history.md) | `GET /project/:projectId/history` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /project/:projectId/tasks` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [List Project Users](actions/list-project-users.md) | `GET /project/:projectId/users` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [List Skills](actions/list-skills.md) | `GET /skills` | [docs](https://www.goodday.work/developers/api-v2/system) |
| [List Statuses](actions/list-statuses.md) | `GET /statuses` | [docs](https://www.goodday.work/developers/api-v2/system) |
| [List Tag Tasks](actions/list-tag-tasks.md) | `GET /tag/:tagId/tasks` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [List Task Messages](actions/list-task-messages.md) | `GET /task/:taskId/messages` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [List Task Types](actions/list-task-types.md) | `GET /task-types` | [docs](https://www.goodday.work/developers/api-v2/system) |
| [List User Action Required Tasks](actions/list-user-action-required-tasks.md) | `GET /user/:userId/action-required-tasks` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [List User Assigned Tasks](actions/list-user-assigned-tasks.md) | `GET /user/:userId/assigned-tasks` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
| [List User Hourly Rate History](actions/list-user-hourly-rate-history.md) | `GET /user/:userId/hourly-rate-history` | [docs](https://www.goodday.work/developers/api-v2/users) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.goodday.work/developers/api-v2/users) |
| [Update Project](actions/update-project.md) | `PUT /project/:projectId` | [docs](https://www.goodday.work/developers/api-v2/projects) |
| [Update Task Status](actions/update-task-status.md) | `PUT /task/:taskId/status` | [docs](https://www.goodday.work/developers/api-v2/tasks) |
