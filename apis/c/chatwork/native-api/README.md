# Chatwork: Native API Reference

A consolidated summary of Chatwork's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.chatwork.com/docs/getting-started
- **API base URL:** `https://api.chatwork.com/v2`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.chatwork.com/packages/oauth2/login.php to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.chatwork.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access users.profile.me:read rooms.all:read rooms.info:read rooms.members:read rooms.messages:read rooms.tasks:read rooms.files:read rooms.all:write rooms:write rooms.info:write rooms.members:write rooms.messages:write rooms.tasks:write rooms.files:write contacts.all:read_write contacts.all:read contacts.all:write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.chatwork.com/token.

[Official authentication documentation](https://developer.chatwork.com/docs/oauth)

### API Token

Authenticate Chatwork requests with an API token sent in the x-chatworktoken header.

### Credentials

- **API Token:** `apiToken` · required · Chatwork API token sent in the x-chatworktoken header.

Send these headers with each API request:

```http
x-chatworktoken: <apiToken>
```

[Official authentication documentation](https://developer.chatwork.com/docs/getting-started)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Chat Task](actions/create-chat-task.md) | `POST /rooms/:room_id/tasks` | [docs](https://developer.chatwork.com/reference/post-rooms-room_id-tasks) |
| [Create Group Chat](actions/create-group-chat.md) | `POST /rooms` | [docs](https://developer.chatwork.com/reference/post-rooms) |
| [Delete Chat Message](actions/delete-chat-message.md) | `DELETE /rooms/:room_id/messages/:message_id` | [docs](https://developer.chatwork.com/reference/delete-rooms-room_id-messages-message_id) |
| [Get Chat](actions/get-chat.md) | `GET /rooms/:room_id` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id) |
| [Get Chat File](actions/get-chat-file.md) | `GET /rooms/:room_id/files/:file_id` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-files-file_id) |
| [Get Chat Message](actions/get-chat-message.md) | `GET /rooms/:room_id/messages/:message_id` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-messages-message_id) |
| [Get Chat Task](actions/get-chat-task.md) | `GET /rooms/:room_id/tasks/:task_id` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-tasks-task_id) |
| [Get My Profile](actions/get-my-profile.md) | `GET /me` | [docs](https://developer.chatwork.com/reference/get-me) |
| [Get My Status](actions/get-my-status.md) | `GET /my/status` | [docs](https://developer.chatwork.com/reference/get-my-status) |
| [Leave or Delete Chat](actions/leave-or-delete-chat.md) | `DELETE /rooms/:room_id` | [docs](https://developer.chatwork.com/reference/delete-rooms-room_id) |
| [List Chat Files](actions/list-chat-files.md) | `GET /rooms/:room_id/files` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-files) |
| [List Chat Members](actions/list-chat-members.md) | `GET /rooms/:room_id/members` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-members) |
| [List Chat Messages](actions/list-chat-messages.md) | `GET /rooms/:room_id/messages` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-messages) |
| [List Chat Tasks](actions/list-chat-tasks.md) | `GET /rooms/:room_id/tasks` | [docs](https://developer.chatwork.com/reference/get-rooms-room_id-tasks) |
| [List Chats](actions/list-chats.md) | `GET /rooms` | [docs](https://developer.chatwork.com/reference/get-rooms) |
| [List My Tasks](actions/list-my-tasks.md) | `GET /my/tasks` | [docs](https://developer.chatwork.com/reference/get-my-tasks) |
| [Mark Message Unread](actions/mark-message-unread.md) | `PUT /rooms/:room_id/messages/unread` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id-messages-unread) |
| [Mark Messages Read](actions/mark-messages-read.md) | `PUT /rooms/:room_id/messages/read` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id-messages-read) |
| [Post Chat Message](actions/post-chat-message.md) | `POST /rooms/:room_id/messages` | [docs](https://developer.chatwork.com/reference/post-rooms-room_id-messages) |
| [Update Chat](actions/update-chat.md) | `PUT /rooms/:room_id` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id) |
| [Update Chat Members](actions/update-chat-members.md) | `PUT /rooms/:room_id/members` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id-members) |
| [Update Chat Message](actions/update-chat-message.md) | `PUT /rooms/:room_id/messages/:message_id` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id-messages-message_id) |
| [Update Chat Task Completion Status](actions/update-chat-task-completion-status.md) | `PUT /rooms/:room_id/tasks/:task_id/status` | [docs](https://developer.chatwork.com/reference/put-rooms-room_id-tasks-task_id-status) |
| [Upload Chat File](actions/upload-chat-file.md) | `POST /rooms/:room_id/files` | [docs](https://developer.chatwork.com/reference/post-rooms-room_id-files) |
