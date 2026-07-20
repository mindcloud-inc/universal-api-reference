# Jostle: Native API Reference

A consolidated summary of Jostle's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://api.jostle.me/docs/getting-started
- **API base URL:** `https://api-prod.jostle.us`

## Authentication

### Tasks API Bearer Token

Use a Jostle Tasks API bearer token for the tenant's Tasks API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.jostle.me/docs/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach File to Task Comment](actions/attach-file-to-task-comment.md) | `POST /v2/tasks/task/:taskId/comment/:commentId/attachment` | [docs](https://api.jostle.me/reference/commentattachment-1) |
| [Comment on Task](actions/comment-on-task.md) | `POST /v2/tasks/task/:id/comment` | [docs](https://api.jostle.me/reference/commenttask-1) |
| [Create Task](actions/create-task.md) | `POST /v2/tasks` | [docs](https://api.jostle.me/reference/posttask-1) |
| [Create Tasks for Many Assignees](actions/create-tasks-for-many-assignees.md) | `POST /v2/tasks/duplicate` | [docs](https://api.jostle.me/reference/duplicatetasks-1) |
| [Get Task](actions/get-task.md) | `GET /v2/tasks/task/:id` | [docs](https://api.jostle.me/reference/gettask-1) |
| [List Enterprise Users](actions/list-enterprise-users.md) | `GET /v2/people` | [docs](https://api.jostle.me/reference/getallusers-1) |
| [List Presets](actions/list-presets.md) | `GET /v2/people/list-presets` | [docs](https://api.jostle.me/reference/getalllistpresets-1) |
| [List Task Comments](actions/list-task-comments.md) | `GET /v2/tasks/task/:id/comments` | [docs](https://api.jostle.me/reference/gettaskcommentslist-1) |
| [Set User Status](actions/set-user-status.md) | `POST /v2/people/status` | [docs](https://api.jostle.me/reference/setuserstatus) |
| [Update Task](actions/update-task.md) | `PATCH /v2/tasks/task/:id` | [docs](https://api.jostle.me/reference/patchtask-1) |
