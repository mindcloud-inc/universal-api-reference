# Kanban Tool: Native API Reference

A consolidated summary of Kanban Tool's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://kanbantool.com/developer/api-v3
- **API base URL:** `https://{domain}.kanbantool.com/api/v3`

## Authentication

### API Key

Authenticate with a Kanban Tool personal access token and account domain.

### Credentials

- **API Key:** `apiKey` · required
- **Account Domain:** `domain` · required · Kanban Tool account domain prefix, for example acme from acme.kanbantool.com.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://kanbantool.com/developer/api-v3)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Task](actions/archive-task.md) | `PATCH /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#archiving-tasks) |
| [Create Attachment](actions/create-attachment.md) | `POST /attachments.json` | [docs](https://kanbantool.com/developer/api-v3#creating-attachments) |
| [Create Comment](actions/create-comment.md) | `POST /tasks/:task_id/comments.json` | [docs](https://kanbantool.com/developer/api-v3#creating-comments) |
| [Create Subtask](actions/create-subtask.md) | `POST /subtasks.json` | [docs](https://kanbantool.com/developer/api-v3#creating-subtasks) |
| [Create Task](actions/create-task.md) | `POST /tasks.json` | [docs](https://kanbantool.com/developer/api-v3#creating-tasks) |
| [Create Time Tracker](actions/create-time-tracker.md) | `POST /time_trackers.json` | [docs](https://kanbantool.com/developer/api-v3#creating-time-trackers) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /tasks/:task_id/comments/:comment_id.json` | [docs](https://kanbantool.com/developer/api-v3#deleting-comments) |
| [Delete Subtask](actions/delete-subtask.md) | `DELETE /subtasks/:subtask_id.json` | [docs](https://kanbantool.com/developer/api-v3#deleting-subtasks) |
| [Delete Task](actions/delete-task.md) | `PATCH /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#deleting-tasks) |
| [Delete Time Tracker](actions/delete-time-tracker.md) | `DELETE /time_trackers/:time_tracker_id.json` | [docs](https://kanbantool.com/developer/api-v3#deleting-time-trackers) |
| [Detach Attachment](actions/detach-attachment.md) | `DELETE /attachments/:attachment_id/detach.json` | [docs](https://kanbantool.com/developer/api-v3#detaching-attachments) |
| [Get Board](actions/get-board.md) | `GET /boards/:board_id/preload.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-boards) |
| [Get Board Details](actions/get-board-details.md) | `GET /boards/:board_id.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-boards-details) |
| [Get Current User](actions/get-current-user.md) | `GET /users/current.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-current-user) |
| [Get Task](actions/get-task.md) | `GET /tasks/:task_id/preload.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-tasks) |
| [Get Task Details](actions/get-task-details.md) | `GET /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-tasks-details) |
| [Get User](actions/get-user.md) | `GET /users/:user_id.json` | [docs](https://kanbantool.com/developer/api-v3#fetching-users) |
| [List Board Changelogs](actions/list-board-changelogs.md) | `GET /boards/:board_id/changelog.json` | [docs](https://kanbantool.com/developer/api-v3#listing-boards-changelogs) |
| [Reorder Subtasks](actions/reorder-subtasks.md) | `PUT /subtasks/reorder.json` | [docs](https://kanbantool.com/developer/api-v3#reordering-subtasks) |
| [Restore Task](actions/restore-task.md) | `PATCH /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#restoring-tasks) |
| [Search Tasks](actions/search-tasks.md) | `GET /tasks/search.json` | [docs](https://kanbantool.com/developer/api-v3#searching-tasks) |
| [Set Attachment Mode](actions/set-attachment-mode.md) | `PATCH /attachments/:attachment_id/set_mode.json` | [docs](https://kanbantool.com/developer/api-v3#attachments-mode) |
| [Unarchive Task](actions/unarchive-task.md) | `PATCH /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#unarchiving-tasks) |
| [Update Subtask](actions/update-subtask.md) | `PATCH /subtasks/:subtask_id.json` | [docs](https://kanbantool.com/developer/api-v3#updating-subtasks) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:task_id.json` | [docs](https://kanbantool.com/developer/api-v3#updating-tasks) |
| [Update Time Tracker](actions/update-time-tracker.md) | `PUT /time_trackers/:time_tracker_id.json` | [docs](https://kanbantool.com/developer/api-v3#updating-time-trackers) |
