# Locu: Native API Reference

A consolidated summary of Locu's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://locu.app/api/docs
- **OpenAPI specification:** https://registry.scalar.com/@locu-labs/apis/locu-public-api/latest
- **API base URL:** `https://api.locu.app/api/v1`

## Authentication

### Personal Access Token

Connect using a Locu personal access token generated from Settings -> API in the Locu workspace.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://locu.app/api/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextCursor`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Timer](actions/cancel-timer.md) | `DELETE /timer` | [docs](https://locu.app/api/docs#tag/timer) |
| [Continue Timer](actions/continue-timer.md) | `POST /timer/continue` | [docs](https://locu.app/api/docs#tag/timer) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://locu.app/api/docs#tag/notes) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://locu.app/api/docs#tag/projects) |
| [Create Session](actions/create-session.md) | `POST /sessions` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Create Session Activity](actions/create-session-activity.md) | `POST /sessions/:id/activities` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://locu.app/api/docs#tag/tasks) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://locu.app/api/docs#tag/webhooks) |
| [Delete Note](actions/delete-note.md) | `DELETE /notes/:id` | [docs](https://locu.app/api/docs#tag/notes) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://locu.app/api/docs#tag/projects) |
| [Delete Session](actions/delete-session.md) | `DELETE /sessions/:id` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Delete Session Activity](actions/delete-session-activity.md) | `DELETE /sessions/:id/activities/:activityId` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://locu.app/api/docs#tag/tasks) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://locu.app/api/docs#tag/account) |
| [Get Note](actions/get-note.md) | `GET /notes/:id` | [docs](https://locu.app/api/docs#tag/notes) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://locu.app/api/docs#tag/projects) |
| [Get Session](actions/get-session.md) | `GET /sessions/:id` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://locu.app/api/docs#tag/tasks) |
| [Get Timer State](actions/get-timer-state.md) | `GET /timer` | [docs](https://locu.app/api/docs#tag/timer) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://locu.app/api/docs#tag/webhooks) |
| [List Activities](actions/list-activities.md) | `GET /sessions/activities` | [docs](https://locu.app/api/docs#tag/sessions) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://locu.app/api/docs#tag/notes) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://locu.app/api/docs#tag/projects) |
| [List Session Activities](actions/list-session-activities.md) | `GET /sessions/:id/activities` | [docs](https://locu.app/api/docs#tag/sessions) |
| [List Sessions](actions/list-sessions.md) | `GET /sessions` | [docs](https://locu.app/api/docs#tag/sessions) |
| [List Subtasks](actions/list-subtasks.md) | `GET /tasks/:id/subtasks` | [docs](https://locu.app/api/docs#tag/tasks) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://locu.app/api/docs#tag/tasks) |
| [List Tasks By Section](actions/list-tasks-by-section.md) | `GET /tasks/sections` | [docs](https://locu.app/api/docs#tag/tasks) |
| [List Webhook Deliveries](actions/list-webhook-deliveries.md) | `GET /webhooks/:id/deliveries` | [docs](https://locu.app/api/docs#tag/webhooks) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://locu.app/api/docs#tag/webhooks) |
| [Pause Timer](actions/pause-timer.md) | `POST /timer/pause` | [docs](https://locu.app/api/docs#tag/timer) |
| [Rotate Webhook Secret](actions/rotate-webhook-secret.md) | `POST /webhooks/:id/rotate-secret` | [docs](https://locu.app/api/docs#tag/webhooks) |
| [Start Timer](actions/start-timer.md) | `POST /timer/start` | [docs](https://locu.app/api/docs#tag/timer) |
| [Stop Timer](actions/stop-timer.md) | `POST /timer/stop` | [docs](https://locu.app/api/docs#tag/timer) |
| [Update Note](actions/update-note.md) | `PATCH /notes/:id` | [docs](https://locu.app/api/docs#tag/notes) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:id` | [docs](https://locu.app/api/docs#tag/projects) |
| [Update Session](actions/update-session.md) | `PATCH /sessions/:id` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Update Session Activity](actions/update-session-activity.md) | `PATCH /sessions/:id/activities/:activityId` | [docs](https://locu.app/api/docs#tag/sessions) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://locu.app/api/docs#tag/tasks) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:id` | [docs](https://locu.app/api/docs#tag/webhooks) |
