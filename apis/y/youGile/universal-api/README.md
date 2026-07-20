# <img src="https://images.mindcloud.co/apps/icons/you-gile_1776781544927.png" alt="YouGile logo" width="28" height="28"> YouGile: Universal API

Manage YouGile projects, tasks, boards, chats, and users

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/youGile/latest
- **Category:** Productivity / Project Management
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yougile.com
- **Vendor API docs:** https://docs.yougile.com/docs/admin-guide/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List tasks](actions/list-tasks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Boards

| Action | Method | Description |
| --- | --- | --- |
| [Create board](actions/create-board.md) | POST | Creates a new board in YouGile. |
| [Get board](actions/get-board.md) | GET | Retrieves details for a board from YouGile. |
| [List boards](actions/list-boards.md) | GET | Retrieves a list of boards from YouGile. |
| [Update board](actions/update-board.md) | PUT | Updates an existing board in YouGile. |

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create column](actions/create-column.md) | POST | Creates a new column in YouGile. |
| [Get column](actions/get-column.md) | GET | Retrieves details for a column from YouGile. |
| [List columns](actions/list-columns.md) | GET | Retrieves a list of columns from YouGile. |
| [Update column](actions/update-column.md) | PUT | Updates an existing column in YouGile. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create group chat](actions/create-group-chat.md) | POST | Creates a new group chat in YouGile. |
| [Get group chat](actions/get-group-chat.md) | GET | Retrieves details for a group chat from YouGile. |
| [List group chats](actions/list-group-chats.md) | GET | Retrieves a list of group chats from YouGile. |
| [Update group chat](actions/update-group-chat.md) | PUT | Updates an existing group chat in YouGile. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create chat message](actions/create-chat-message.md) | POST | Creates a chat message in YouGile. |
| [Get chat message](actions/get-chat-message.md) | GET | Retrieves a chat message from YouGile. |
| [List chat messages](actions/list-chat-messages.md) | GET | Retrieves chat messages from a YouGile chat. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create project](actions/create-project.md) | POST | Creates a new project in YouGile. |
| [Get project](actions/get-project.md) | GET | Retrieves details for a project from YouGile. |
| [List projects](actions/list-projects.md) | GET | Retrieves a list of projects from YouGile. |
| [Update project](actions/update-project.md) | PUT | Updates an existing project in YouGile. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create task](actions/create-task.md) | POST | Creates a new task in YouGile. |
| [Get task](actions/get-task.md) | GET | Retrieves details for a task from YouGile. |
| [List recent tasks](actions/list-recent-tasks.md) | GET | Retrieves recent tasks from YouGile in reverse order. |
| [List tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from YouGile. |
| [Update task](actions/update-task.md) | PUT | Updates an existing task in YouGile. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get user](actions/get-user.md) | GET | Retrieves details for a user from YouGile. |
| [List users](actions/list-users.md) | GET | Retrieves a list of users from YouGile. |

