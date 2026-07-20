# <img src="https://images.mindcloud.co/apps/icons/kanban-tool_1774444601012.png" alt="Kanban Tool logo" width="28" height="28"> Kanban Tool: Universal API

Manage boards, tasks, subtasks, comments, attachments, and time tracking

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kanbanTool/latest
- **Category:** Productivity / Project Management
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kanbantool.com
- **Vendor API docs:** https://kanbantool.com/developer/api-v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanTool/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Create Attachment](actions/create-attachment.md) | POST |  |
| [Detach Attachment](actions/detach-attachment.md) | DELETE |  |
| [Set Attachment Mode](actions/set-attachment-mode.md) | PUT |  |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Board](actions/get-board.md) | GET |  |
| [Get Board Details](actions/get-board-details.md) | GET |  |

### Changelog

| Action | Method | Description |
| --- | --- | --- |
| [List Board Changelogs](actions/list-board-changelogs.md) | GET |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | POST |  |
| [Delete Comment](actions/delete-comment.md) | DELETE |  |

### Subtask

| Action | Method | Description |
| --- | --- | --- |
| [Create Subtask](actions/create-subtask.md) | POST |  |
| [Delete Subtask](actions/delete-subtask.md) | DELETE |  |
| [Reorder Subtasks](actions/reorder-subtasks.md) | PUT |  |
| [Update Subtask](actions/update-subtask.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Archive Task](actions/archive-task.md) | PUT |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | PUT |  |
| [Get Task](actions/get-task.md) | GET |  |
| [Get Task Details](actions/get-task-details.md) | GET |  |
| [Restore Task](actions/restore-task.md) | PUT |  |
| [Search Tasks](actions/search-tasks.md) | GET |  |
| [Unarchive Task](actions/unarchive-task.md) | PUT |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Time Tracker

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Tracker](actions/create-time-tracker.md) | POST |  |
| [Delete Time Tracker](actions/delete-time-tracker.md) | DELETE |  |
| [Update Time Tracker](actions/update-time-tracker.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |

