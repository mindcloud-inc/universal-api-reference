# Twist: Native API Reference

A consolidated summary of Twist's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.twist.com/v3/
- **API base URL:** `https://api.twist.com/api/v3`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://twist.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://twist.com/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `user:read,workspaces:read,channels:read,channels:write,threads:read,threads:write,comments:read,comments:write,messages:read,messages:write,attachments:write,search:read`.

[Official authentication documentation](https://developer.twist.com/v3/#authorization)

## Pagination

Use `limit` in the query string to set the page size.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Channel](actions/archive-channel.md) | `POST /channels/archive` | [docs](https://developer.twist.com/v3/#archive-channel) |
| [Create Channel](actions/create-channel.md) | `POST /channels/add` | [docs](https://developer.twist.com/v3/#add-channel) |
| [Create Comment](actions/create-comment.md) | `POST /comments/add` | [docs](https://developer.twist.com/v3/#add-comment) |
| [Create Message](actions/create-message.md) | `POST /conversation_messages/add` | [docs](https://developer.twist.com/v3/#add-message-to-conversation) |
| [Create Thread](actions/create-thread.md) | `POST /threads/add` | [docs](https://developer.twist.com/v3/#add-thread) |
| [Get Channel](actions/get-channel.md) | `GET /channels/getone` | [docs](https://developer.twist.com/v3/#get-channel) |
| [Get Current User](actions/get-current-user.md) | `GET /users/get_session_user` | [docs](https://developer.twist.com/v3/#get-current-user) |
| [Get Default Workspace](actions/get-default-workspace.md) | `GET /workspaces/get_default` | [docs](https://developer.twist.com/v3/#get-default-workspace) |
| [Get or Create Conversation](actions/get-or-create-conversation.md) | `POST /conversations/get_or_create` | [docs](https://developer.twist.com/v3/#get-or-create-conversation) |
| [Get Thread](actions/get-thread.md) | `GET /threads/getone` | [docs](https://developer.twist.com/v3/#get-thread) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/getone` | [docs](https://developer.twist.com/v3/#get-workspace) |
| [List Channels](actions/list-channels.md) | `GET /channels/get` | [docs](https://developer.twist.com/v3/#get-all-channels) |
| [List Comments](actions/list-comments.md) | `GET /comments/get` | [docs](https://developer.twist.com/v3/#get-all-comments) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations/get` | [docs](https://developer.twist.com/v3/#get-all-conversations) |
| [List Messages](actions/list-messages.md) | `GET /conversation_messages/get` | [docs](https://developer.twist.com/v3/#get-all-messages) |
| [List Threads](actions/list-threads.md) | `GET /threads/get` | [docs](https://developer.twist.com/v3/#get-all-threads) |
| [List Unread Threads](actions/list-unread-threads.md) | `GET /threads/get_unread` | [docs](https://developer.twist.com/v3/#get-unread-threads) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces/get` | [docs](https://developer.twist.com/v3/#get-all-workspaces) |
| [Mark Thread as Read](actions/mark-thread-as-read.md) | `POST /threads/mark_read` | [docs](https://developer.twist.com/v3/#mark-thread-as-read) |
| [Move Thread to Channel](actions/move-thread-to-channel.md) | `POST /threads/move_to_channel` | [docs](https://developer.twist.com/v3/#move-thread) |
| [Search Content](actions/search-content.md) | `GET /search` | [docs](https://developer.twist.com/v3/#search-for-query) |
| [Update Channel](actions/update-channel.md) | `POST /channels/update` | [docs](https://developer.twist.com/v3/#update-channel) |
| [Update Thread](actions/update-thread.md) | `POST /threads/update` | [docs](https://developer.twist.com/v3/#update-thread) |
| [Upload Attachment](actions/upload-attachment.md) | `POST /attachments/upload` | [docs](https://developer.twist.com/v3/#upload-an-attachment) |
