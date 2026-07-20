# <img src="https://images.mindcloud.co/apps/icons/2fd452a6-4925-4f42-8c9d-9948242eb9da-3_1777051709481.png" alt="KanbanFlow logo" width="28" height="28"> KanbanFlow: Universal API

Manage KanbanFlow boards, tasks, users, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kanbanFlow/latest
- **Category:** Productivity / Project Management
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kanbanflow.com
- **Vendor API docs:** https://kanbanflow.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get board](actions/get-board.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kanbanFlow/latest/actions/get-board?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Get board](actions/get-board.md) | GET | Retrieves the structure of a KanbanFlow board. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Add comment](actions/add-comment.md) | POST | Creates a new comment on a KanbanFlow task. |
| [Delete comment](actions/delete-comment.md) | DELETE | Deletes an existing comment from a KanbanFlow task. |
| [Get comments](actions/get-comments.md) | GET | Retrieves all comments for a KanbanFlow task. |
| [Update comment](actions/update-comment.md) | PUT | Updates an existing comment on a KanbanFlow task. |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create label](actions/create-label.md) | POST | Creates a new label on a KanbanFlow task. |
| [Delete label](actions/delete-label.md) | DELETE | Deletes an existing label from a KanbanFlow task. |
| [Update label](actions/update-label.md) | PUT | Updates an existing label on a KanbanFlow task. |

### Subtasks

| Action | Method | Description |
| --- | --- | --- |
| [Create subtask](actions/create-subtask.md) | POST | Creates a new subtask in KanbanFlow. |
| [Delete subtask](actions/delete-subtask.md) | DELETE | Deletes an existing subtask from KanbanFlow. |
| [Update subtask](actions/update-subtask.md) | PUT | Updates an existing subtask in KanbanFlow. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST | Creates a new task in KanbanFlow. |
| [Delete task](actions/delete-task.md) | DELETE | Deletes an existing task from KanbanFlow. |
| [Get task by ID](actions/get-task-by-id.md) | GET | Retrieves a task from KanbanFlow by ID. |
| [Get tasks by column](actions/get-tasks-by-column.md) | GET | Retrieves tasks from a KanbanFlow column. |
| [Update task](actions/update-task.md) | PUT | Updates an existing task in KanbanFlow. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Add manual time entry](actions/add-manual-time-entry.md) | POST | Creates a new manual time entry in KanbanFlow. |
| [Delete manual time entry](actions/delete-manual-time-entry.md) | DELETE | Deletes an existing manual time entry from KanbanFlow. |
| [Get board time entries](actions/get-board-time-entries.md) | GET | Retrieves board time entries from KanbanFlow for a time period. |
| [Get manual time entries](actions/get-manual-time-entries.md) | GET | Retrieves all manual time entries for a KanbanFlow task. |
| [Update manual time entry](actions/update-manual-time-entry.md) | PUT | Updates an existing manual time entry in KanbanFlow. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get users](actions/get-users.md) | GET | Retrieves all users on a KanbanFlow board. |

