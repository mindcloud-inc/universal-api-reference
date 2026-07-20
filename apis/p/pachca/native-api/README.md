# Pachca: Native API Reference

A consolidated summary of Pachca's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://dev.pachca.com/guides/authorization
- **OpenAPI specification:** https://github.com/pachca/openapi/blob/main/packages/spec/openapi.en.yaml
- **API base URL:** `https://api.pachca.com/api/shared/v1`

## Authentication

### API token

Bearer token authentication for the Pachca API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dev.pachca.com/guides/authorization)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create chat](actions/create-chat.md) | `POST /chats` | [docs](https://dev.pachca.com/reference/chats-create) |
| [Create message](actions/create-message.md) | `POST /messages` | [docs](https://dev.pachca.com/reference/messages-create) |
| [Create task](actions/create-task.md) | `POST /tasks` | [docs](https://dev.pachca.com/reference/tasks-create) |
| [Delete message](actions/delete-message.md) | `DELETE /messages/{id}` | [docs](https://dev.pachca.com/reference/messages-id-delete) |
| [Delete task](actions/delete-task.md) | `DELETE /tasks/{id}` | [docs](https://dev.pachca.com/reference/tasks-id-delete) |
| [Get chat](actions/get-chat.md) | `GET /chats/{id}` | [docs](https://dev.pachca.com/reference/chats-id) |
| [Get group tag](actions/get-group-tag.md) | `GET /group_tags/{id}` | [docs](https://dev.pachca.com/reference/group-tags-id) |
| [Get message](actions/get-message.md) | `GET /messages/{id}` | [docs](https://dev.pachca.com/reference/messages-id) |
| [Get profile](actions/get-profile.md) | `GET /profile` | [docs](https://dev.pachca.com/reference/profile) |
| [Get profile status](actions/get-profile-status.md) | `GET /profile/status` | [docs](https://dev.pachca.com/reference/profile-status) |
| [Get task](actions/get-task.md) | `GET /tasks/{id}` | [docs](https://dev.pachca.com/reference/tasks-id) |
| [Get thread](actions/get-thread.md) | `GET /threads/{id}` | [docs](https://dev.pachca.com/reference/threads-id) |
| [Get token info](actions/get-token-info.md) | `GET /oauth/token/info` | [docs](https://dev.pachca.com/reference/oauth-token-info) |
| [Get user](actions/get-user.md) | `GET /users/{id}` | [docs](https://dev.pachca.com/reference/users-id) |
| [List chat members](actions/list-chat-members.md) | `GET /chats/{id}/members` | [docs](https://dev.pachca.com/reference/chats-id-members) |
| [List chats](actions/list-chats.md) | `GET /chats` | [docs](https://dev.pachca.com/reference/chats) |
| [List custom properties](actions/list-custom-properties.md) | `GET /custom_properties` | [docs](https://dev.pachca.com/reference/custom-properties) |
| [List group tag users](actions/list-group-tag-users.md) | `GET /group_tags/{id}/users` | [docs](https://dev.pachca.com/reference/group-tags-id-users) |
| [List group tags](actions/list-group-tags.md) | `GET /group_tags` | [docs](https://dev.pachca.com/reference/group-tags) |
| [List message reactions](actions/list-message-reactions.md) | `GET /messages/{id}/reactions` | [docs](https://dev.pachca.com/reference/messages-id-reactions) |
| [List message read member IDs](actions/list-message-read-member-ids.md) | `GET /messages/{id}/read_member_ids` | [docs](https://dev.pachca.com/reference/messages-id-read-member-ids) |
| [List messages](actions/list-messages.md) | `GET /messages` | [docs](https://dev.pachca.com/reference/messages) |
| [List tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://dev.pachca.com/reference/tasks) |
| [List users](actions/list-users.md) | `GET /users` | [docs](https://dev.pachca.com/reference/users) |
| [Search chats](actions/search-chats.md) | `GET /search/chats` | [docs](https://dev.pachca.com/reference/search-chats) |
| [Search messages](actions/search-messages.md) | `GET /search/messages` | [docs](https://dev.pachca.com/reference/search-messages) |
| [Search users](actions/search-users.md) | `GET /search/users` | [docs](https://dev.pachca.com/reference/search-users) |
| [Update message](actions/update-message.md) | `PUT /messages/{id}` | [docs](https://dev.pachca.com/reference/messages-id-update) |
| [Update task](actions/update-task.md) | `PUT /tasks/{id}` | [docs](https://dev.pachca.com/reference/tasks-id-update) |
