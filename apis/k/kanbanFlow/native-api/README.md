# KanbanFlow: Native API Reference

A consolidated summary of KanbanFlow's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://kanbanflow.com/api-docs
- **API base URL:** `https://kanbanflow.com/api/v1`

## Authentication

### API Token

Authenticate with a KanbanFlow API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://kanbanflow.com/api-docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add comment](actions/add-comment.md) | `POST /tasks/:taskId/comments` | [docs](https://kanbanflow.com/api-docs/add-comment) |
| [Add manual time entry](actions/add-manual-time-entry.md) | `POST /tasks/:taskId/manual-time-entries` | [docs](https://kanbanflow.com/api-docs/add-manual-time-entry) |
| [Create label](actions/create-label.md) | `POST /tasks/:taskId/labels` | [docs](https://kanbanflow.com/api-docs/create-label) |
| [Create subtask](actions/create-subtask.md) | `POST /tasks/:taskId/subtasks` | [docs](https://kanbanflow.com/api-docs/create-subtask) |
| [Create task](actions/create-task.md) | `POST /tasks` | [docs](https://kanbanflow.com/api-docs/create-task) |
| [Delete comment](actions/delete-comment.md) | `DELETE /tasks/:taskId/comments/:commentId` | [docs](https://kanbanflow.com/api-docs/delete-comment) |
| [Delete label](actions/delete-label.md) | `DELETE /tasks/:taskId/labels/by-name/:labelName` | [docs](https://kanbanflow.com/api-docs/delete-label) |
| [Delete manual time entry](actions/delete-manual-time-entry.md) | `DELETE /tasks/:taskId/manual-time-entries/:manualTimeEntryId` | [docs](https://kanbanflow.com/api-docs/delete-manual-time-entry) |
| [Delete subtask](actions/delete-subtask.md) | `DELETE /tasks/:taskId/subtasks/by-index/:index` | [docs](https://kanbanflow.com/api-docs/delete-subtask) |
| [Delete task](actions/delete-task.md) | `DELETE /tasks/:taskId` | [docs](https://kanbanflow.com/api-docs/delete-task) |
| [Get board](actions/get-board.md) | `GET /board` | [docs](https://kanbanflow.com/api-docs/get-board) |
| [Get board time entries](actions/get-board-time-entries.md) | `GET /time-entries` | [docs](https://kanbanflow.com/api-docs/time-entries) |
| [Get comments](actions/get-comments.md) | `GET /tasks/:taskId/comments` | [docs](https://kanbanflow.com/api-docs/get-comments) |
| [Get manual time entries](actions/get-manual-time-entries.md) | `GET /tasks/:taskId/manual-time-entries` | [docs](https://kanbanflow.com/api-docs/get-manual-time-entries) |
| [Get task by ID](actions/get-task-by-id.md) | `GET /tasks/:taskId` | [docs](https://kanbanflow.com/api-docs/get-tasks) |
| [Get tasks by column](actions/get-tasks-by-column.md) | `GET /tasks` | [docs](https://kanbanflow.com/api-docs/get-tasks) |
| [Get users](actions/get-users.md) | `GET /users` | [docs](https://kanbanflow.com/api-docs/get-users) |
| [Update comment](actions/update-comment.md) | `POST /tasks/:taskId/comments/:commentId` | [docs](https://kanbanflow.com/api-docs/update-comment) |
| [Update label](actions/update-label.md) | `POST /tasks/:taskId/labels/by-name/:labelName` | [docs](https://kanbanflow.com/api-docs/update-label) |
| [Update manual time entry](actions/update-manual-time-entry.md) | `POST /tasks/:taskId/manual-time-entries/:manualTimeEntryId` | [docs](https://kanbanflow.com/api-docs/update-manual-time-entry) |
| [Update subtask](actions/update-subtask.md) | `POST /tasks/:taskId/subtasks/by-index/:index` | [docs](https://kanbanflow.com/api-docs/update-subtask) |
| [Update task](actions/update-task.md) | `POST /tasks/:taskId` | [docs](https://kanbanflow.com/api-docs/update-task) |
