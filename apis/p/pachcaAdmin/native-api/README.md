# Pachca (Admin): Native API Reference

A consolidated summary of Pachca (Admin)'s API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://dev.pachca.com
- **OpenAPI specification:** https://dev.pachca.com/openapi.yaml
- **API base URL:** `https://api.pachca.com/api/shared/v1`

## Authentication

### Personal access token

Use a Pachca personal token with the required scopes.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.pachca.com/api/authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–50). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Chat Group Tags](actions/add-chat-group-tags.md) | `POST /chats/:id/group_tags` | [docs](https://dev.pachca.com/api/members/add-tags) |
| [Add Chat Members](actions/add-chat-members.md) | `POST /chats/:id/members` | [docs](https://dev.pachca.com/api/members/add) |
| [Add Reaction](actions/add-reaction.md) | `POST /messages/:id/reactions` | [docs](https://dev.pachca.com/api/reactions/add) |
| [Archive Chat](actions/archive-chat.md) | `PUT /chats/:id/archive` | [docs](https://dev.pachca.com/api/chats/archive) |
| [Clear Current Status](actions/clear-user-status.md) | `DELETE /profile/status` | [docs](https://dev.pachca.com/api/profile/delete-status) |
| [Create Chat](actions/create-chat.md) | `POST /chats` | [docs](https://dev.pachca.com/api/chats/create) |
| [Create Group Tag](actions/create-group-tag.md) | `POST /group_tags` | [docs](https://dev.pachca.com/api/group-tags/create) |
| [Create Message](actions/create-message.md) | `POST /messages` | [docs](https://dev.pachca.com/api/messages/create) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://dev.pachca.com/tasks/create) |
| [Create Thread](actions/create-thread.md) | `POST /messages/:id/thread` | [docs](https://dev.pachca.com/api/threads/add) |
| [Delete Group Tag](actions/delete-group-tag.md) | `DELETE /group_tags/:id` | [docs](https://dev.pachca.com/api/group-tags/delete) |
| [Delete Message](actions/delete-message.md) | `DELETE /messages/:id` | [docs](https://dev.pachca.com/api/messages/delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://dev.pachca.com/api/tasks/delete) |
| [Get Chat](actions/get-chat.md) | `GET /chats/:id` | [docs](https://dev.pachca.com/api/chats/get) |
| [Get Chat Export](actions/get-chat-export.md) | `GET /chats/exports/:id` | [docs](https://dev.pachca.com/api/common/request-export) |
| [Get Group Tag](actions/get-group-tag.md) | `GET /group_tags/:id` | [docs](https://dev.pachca.com/api/group-tags/get) |
| [Get Message](actions/get-message.md) | `GET /messages/:id` | [docs](https://dev.pachca.com/api/messages/get) |
| [Get Profile](actions/get-profile.md) | `GET /profile` | [docs](https://dev.pachca.com/api/profile/get) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://dev.pachca.com/api/tasks/get) |
| [Get Thread](actions/get-thread.md) | `GET /threads/:id` | [docs](https://dev.pachca.com/api/threads/get) |
| [Get Token Info](actions/get-token-info.md) | `GET /oauth/token/info` | [docs](https://dev.pachca.com/api/authorization) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://dev.pachca.com/api/users/get) |
| [Get Current Status](actions/get-user-status.md) | `GET /profile/status` | [docs](https://dev.pachca.com/api/profile/get-status) |
| [List Audit Events](actions/list-audit-events.md) | `GET /audit_events` | [docs](https://dev.pachca.com/api/security/list) |
| [List Chat Members](actions/list-chat-members.md) | `GET /chats/:id/members` | [docs](https://dev.pachca.com/api/members/list) |
| [List Chats](actions/list-chats.md) | `GET /chats` | [docs](https://dev.pachca.com/api/chats/list) |
| [List Group Tag Users](actions/list-group-tag-users.md) | `GET /group_tags/:id/users` | [docs](https://dev.pachca.com/api/group-tags/get-users) |
| [List Group Tags](actions/list-group-tags.md) | `GET /group_tags` | [docs](https://dev.pachca.com/api/group-tags/list) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://dev.pachca.com/api/messages/list) |
| [List Reactions](actions/list-reactions.md) | `GET /messages/:id/reactions` | [docs](https://dev.pachca.com/api/reactions/list) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://dev.pachca.com/api/tasks/list) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://dev.pachca.com/api/users/list) |
| [Remove Chat Group Tag](actions/remove-chat-group-tag.md) | `DELETE /chats/:id/group_tags/:tag_id` | [docs](https://dev.pachca.com/api/members/remove-tag) |
| [Remove Chat Member](actions/remove-chat-member.md) | `DELETE /chats/:id/members/:user_id` | [docs](https://dev.pachca.com/api/members/remove) |
| [Remove Reaction](actions/remove-reaction.md) | `DELETE /messages/:id/reactions` | [docs](https://dev.pachca.com/api/reactions/remove) |
| [Request Chat Export](actions/request-chat-export.md) | `POST /chats/exports` | [docs](https://dev.pachca.com/api/common/request-export) |
| [Search Chats](actions/search-chats.md) | `GET /search/chats` | [docs](https://dev.pachca.com/search/list-chats) |
| [Search Messages](actions/search-messages.md) | `GET /search/messages` | [docs](https://dev.pachca.com/search/list-messages) |
| [Search Users](actions/search-users.md) | `GET /search/users` | [docs](https://dev.pachca.com/search/list-users) |
| [Set Current Status](actions/set-user-status.md) | `PUT /profile/status` | [docs](https://dev.pachca.com/api/profile/update-status) |
| [Unarchive Chat](actions/unarchive-chat.md) | `PUT /chats/:id/unarchive` | [docs](https://dev.pachca.com/api/chats/unarchive) |
| [Update Chat](actions/update-chat.md) | `PUT /chats/:id` | [docs](https://dev.pachca.com/api/chats/update) |
| [Update Chat Member Role](actions/update-chat-member-role.md) | `PUT /chats/:id/members/:user_id` | [docs](https://dev.pachca.com/api/members/update-role) |
| [Update Group Tag](actions/update-group-tag.md) | `PUT /group_tags/:id` | [docs](https://dev.pachca.com/api/group-tags/update) |
| [Update Message](actions/update-message.md) | `PUT /messages/:id` | [docs](https://dev.pachca.com/api/messages/update) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://dev.pachca.com/api/tasks/update) |
