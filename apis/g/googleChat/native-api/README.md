# Google Chat: Native API Reference

A consolidated summary of Google Chat's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/chat/api/reference/rest
- **API base URL:** `https://chat.googleapis.com/v1`

## Authentication

### OAuth 2.0

Connect Google Chat with your Google account.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile https://www.googleapis.com/auth/chat.messages.create https://www.googleapis.com/auth/chat.spaces.readonly https://www.googleapis.com/auth/chat.memberships.readonly`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/workspace/chat/authenticate-authorize-chat-user)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Response data is read from `spaces`. The next-page cursor is read from `nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; maximum 1000). Use `pageToken` in the query string as the pagination cursor.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | `POST /spaces/:space/messages` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.messages/create) |
| [Find Direct Message](actions/find-direct-message.md) | `GET /spaces\:findDirectMessage` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/findDirectMessage) |
| [Get Membership](actions/get-membership.md) | `GET /spaces/:space/members/:member` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.members/get) |
| [Get Space](actions/get-space.md) | `GET /spaces/:space` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/get) |
| [List Memberships](actions/list-memberships.md) | `GET /spaces/:space/members` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces.members/list) |
| [List Spaces](actions/list-spaces.md) | `GET /spaces` | [docs](https://developers.google.com/workspace/chat/api/reference/rest/v1/spaces/list) |
