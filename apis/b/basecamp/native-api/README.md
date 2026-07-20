# Basecamp: Native API Reference

A consolidated summary of Basecamp's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://github.com/basecamp/bc3-api
- **OpenAPI specification:** https://raw.githubusercontent.com/basecamp/basecamp-sdk/main/openapi.json
- **API base URL:** `https://3.basecampapi.com`

## Authentication

### OAuth 2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://launchpad.37signals.com/authorization/new to approve access.
2. Exchange the returned authorization code with a POST request to https://launchpad.37signals.com/authorization/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `__no_scope__`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://launchpad.37signals.com/authorization/token.

[Official authentication documentation](https://github.com/basecamp/api/blob/master/sections/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `User-Agent` | `MindCloud (apps@mindcloud.co)` |

Responses from this API use JSON.

## Pagination

Pages are numbered from 1. Follow the complete next-page URL returned by the API.

## Retry behavior

Retry responses with status codes `429,503`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Todo](actions/complete-todo.md) | `POST /:accountId/todos/:todoId/completion.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#complete-a-to-do) |
| [Create Document](actions/create-document.md) | `POST /:accountId/vaults/:vaultId/documents.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#create-a-document) |
| [Create Message](actions/create-message.md) | `POST /:accountId/message_boards/:boardId/messages.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#create-a-message) |
| [Create Todo](actions/create-todo.md) | `POST /:accountId/todolists/:todolistId/todos.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#create-a-to-do) |
| [Create Todolist](actions/create-todolist.md) | `POST /:accountId/todosets/:todosetId/todolists.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#create-a-to-do-list) |
| [Get Authorization](actions/get-authorization.md) | `GET https://launchpad.37signals.com/authorization.json` | [docs](https://github.com/basecamp/api/blob/master/sections/authentication.md) |
| [Get Document](actions/get-document.md) | `GET /:accountId/documents/:documentId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#get-a-document) |
| [Get Message](actions/get-message.md) | `GET /:accountId/messages/:messageId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#get-a-message) |
| [Get Message Board](actions/get-message-board.md) | `GET /:accountId/message_boards/:boardId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/message_boards.md#get-message-board) |
| [Get Person](actions/get-person.md) | `GET /:accountId/people/:personId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/people.md#get-person) |
| [Get Project](actions/get-project.md) | `GET /:accountId/projects/:projectId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/projects.md#get-a-project) |
| [Get Todo](actions/get-todo.md) | `GET /:accountId/todos/:todoId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#get-a-to-do) |
| [Get Todolist](actions/get-todolist.md) | `GET /:accountId/todolists/:id.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#get-a-to-do-list) |
| [Get Todoset](actions/get-todoset.md) | `GET /:accountId/todosets/:todosetId.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todosets.md#get-to-do-set) |
| [List Documents](actions/list-documents.md) | `GET /:accountId/vaults/:vaultId/documents.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/documents.md#get-documents) |
| [List Messages](actions/list-messages.md) | `GET /:accountId/message_boards/:boardId/messages.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/messages.md#get-messages) |
| [List People](actions/list-people.md) | `GET /:accountId/people.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/people.md#get-all-people) |
| [List Project People](actions/list-project-people.md) | `GET /:accountId/projects/:projectId/people.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/people.md#get-people-on-a-project) |
| [List Projects](actions/list-projects.md) | `GET /:accountId/projects.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/projects.md#get-all-projects) |
| [List Recordings](actions/list-recordings.md) | `GET /:accountId/projects/recordings.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/recordings.md#get-recordings) |
| [List Todolists](actions/list-todolists.md) | `GET /:accountId/todosets/:todosetId/todolists.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todolists.md#get-to-do-lists) |
| [List Todos](actions/list-todos.md) | `GET /:accountId/todolists/:todolistId/todos.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/todos.md#get-to-dos) |
| [List Uploads](actions/list-uploads.md) | `GET /:accountId/vaults/:vaultId/uploads.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/uploads.md#get-uploads) |
| [Search Recordings](actions/search-recordings.md) | `GET /:accountId/search.json` | [docs](https://github.com/basecamp/bc3-api/blob/master/sections/search.md#search-recordings) |
