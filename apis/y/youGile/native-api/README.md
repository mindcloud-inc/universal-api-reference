# YouGile: Native API Reference

A consolidated summary of YouGile's API configuration and 26 documented operations, with links to official documentation.

- **Official docs:** https://docs.yougile.com/docs/admin-guide/api/
- **OpenAPI specification:** https://ru.yougile.com/api-json
- **API base URL:** `{companyDomain}/api-v2`

## Authentication

### API Key

Connect with a YouGile API key and company domain.

### Credentials

- **API Key:** `apiKey` · required
- **Company Domain:** `companyDomain` · required · Your YouGile company base URL (for example, https://mindcloud.yougile.com).

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.yougile.com/docs/admin-guide/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (26 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create board](actions/create-board.md) | `POST /boards` | [docs](https://ru.yougile.com/api-v2#/operations/BoardController_create) |
| [Create chat message](actions/create-chat-message.md) | `POST /chats/:chatId/messages` | [docs](https://ru.yougile.com/api-v2#/operations/ChatMessageController_sendMessage) |
| [Create column](actions/create-column.md) | `POST /columns` | [docs](https://ru.yougile.com/api-v2#/operations/ColumnController_create) |
| [Create group chat](actions/create-group-chat.md) | `POST /group-chats` | [docs](https://ru.yougile.com/api-v2#/operations/GroupChatController_create) |
| [Create project](actions/create-project.md) | `POST /projects` | [docs](https://ru.yougile.com/api-v2#/operations/ProjectController_create) |
| [Create task](actions/create-task.md) | `POST /tasks` | [docs](https://ru.yougile.com/api-v2#/operations/TaskController_create) |
| [Get board](actions/get-board.md) | `GET /boards/:id` | [docs](https://ru.yougile.com/api-v2#/operations/BoardController_get) |
| [Get chat message](actions/get-chat-message.md) | `GET /chats/:chatId/messages/:id` | [docs](https://ru.yougile.com/api-v2#/operations/ChatMessageController_get) |
| [Get column](actions/get-column.md) | `GET /columns/:id` | [docs](https://ru.yougile.com/api-v2#/operations/ColumnController_get) |
| [Get group chat](actions/get-group-chat.md) | `GET /group-chats/:id` | [docs](https://ru.yougile.com/api-v2#/operations/GroupChatController_get) |
| [Get project](actions/get-project.md) | `GET /projects/:id` | [docs](https://ru.yougile.com/api-v2#/operations/ProjectController_get) |
| [Get task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://ru.yougile.com/api-v2#/operations/TaskController_get) |
| [Get user](actions/get-user.md) | `GET /users/:id` | [docs](https://ru.yougile.com/api-v2#/operations/UserController_get) |
| [List boards](actions/list-boards.md) | `GET /boards` | [docs](https://ru.yougile.com/api-v2#/operations/BoardController_search) |
| [List chat messages](actions/list-chat-messages.md) | `GET /chats/:chatId/messages` | [docs](https://ru.yougile.com/api-v2#/operations/ChatMessageController_search) |
| [List columns](actions/list-columns.md) | `GET /columns` | [docs](https://ru.yougile.com/api-v2#/operations/ColumnController_search) |
| [List group chats](actions/list-group-chats.md) | `GET /group-chats` | [docs](https://ru.yougile.com/api-v2#/operations/GroupChatController_search) |
| [List projects](actions/list-projects.md) | `GET /projects` | [docs](https://ru.yougile.com/api-v2#/operations/ProjectController_search) |
| [List recent tasks](actions/list-recent-tasks.md) | `GET /tasks` | [docs](https://ru.yougile.com/api-v2#/operations/TaskController_searchReversed) |
| [List tasks](actions/list-tasks.md) | `GET /task-list` | [docs](https://ru.yougile.com/api-v2#/operations/TaskController_search) |
| [List users](actions/list-users.md) | `GET /users` | [docs](https://ru.yougile.com/api-v2#/operations/UserController_search) |
| [Update board](actions/update-board.md) | `PUT /boards/:id` | [docs](https://ru.yougile.com/api-v2#/operations/BoardController_update) |
| [Update column](actions/update-column.md) | `PUT /columns/:id` | [docs](https://ru.yougile.com/api-v2#/operations/ColumnController_update) |
| [Update group chat](actions/update-group-chat.md) | `PUT /group-chats/:id` | [docs](https://ru.yougile.com/api-v2#/operations/GroupChatController_update) |
| [Update project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://ru.yougile.com/api-v2#/operations/ProjectController_update) |
| [Update task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://ru.yougile.com/api-v2#/operations/TaskController_update) |
