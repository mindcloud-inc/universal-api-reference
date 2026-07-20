# XenForo: Native API Reference

A consolidated summary of XenForo's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.xenforo.com/api
- **OpenAPI specification:** https://docs.xenforo.com/api/openapi.json
- **API base URL:** `{baseUrl}/2310/api`

## Authentication

### XenForo API Key

Authenticate XenForo REST API requests with a XenForo API key sent in the XF-Api-Key header.

### Credentials

- **API Key:** `apiKey` · required · XenForo API key generated in the XenForo Admin Control Panel at Setup > Service providers > API keys.
- **API User ID:** `apiUserId` · optional · Optional user ID sent as XF-Api-User. Super-user API keys use this to choose the XenForo user the request acts as.
- **XenForo Installation URL:** `baseUrl` · required · Base URL of the XenForo installation. Include any subdirectory where XenForo is installed, but do not include /api.

[Official authentication documentation](https://docs.xenforo.com/manual/reference/rest-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Thread Reply](actions/add-thread-reply.md) | `POST /posts/` | [docs](https://docs.xenforo.com/api/post-posts) |
| [Create Thread](actions/create-thread.md) | `POST /threads/` | [docs](https://docs.xenforo.com/api/post-threads) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:id/` | [docs](https://docs.xenforo.com/api/delete-posts-id) |
| [Get Alert](actions/get-alert.md) | `GET /alerts/:id/` | [docs](https://docs.xenforo.com/api/get-alerts-id) |
| [Get Alerts](actions/get-alerts.md) | `GET /alerts/` | [docs](https://docs.xenforo.com/api/get-alerts) |
| [Get Current User](actions/get-current-user.md) | `GET /me/` | [docs](https://docs.xenforo.com/api/get-me) |
| [Get Flattened Node Tree](actions/get-flattened-node-tree.md) | `GET /nodes/flattened` | [docs](https://docs.xenforo.com/api/get-nodes-flattened) |
| [Get Forum](actions/get-forum.md) | `GET /forums/:id/` | [docs](https://docs.xenforo.com/api/get-forums-id) |
| [Get Forum Threads](actions/get-forum-threads.md) | `GET /forums/:id/threads` | [docs](https://docs.xenforo.com/api/get-forums-id-threads) |
| [Get Node](actions/get-node.md) | `GET /nodes/:id/` | [docs](https://docs.xenforo.com/api/get-nodes-id) |
| [Get Node Tree](actions/get-node-tree.md) | `GET /nodes/` | [docs](https://docs.xenforo.com/api/get-nodes) |
| [Get Post](actions/get-post.md) | `GET /posts/:id/` | [docs](https://docs.xenforo.com/api/get-posts-id) |
| [Get Site Info](actions/get-site-info.md) | `GET /index/` | [docs](https://docs.xenforo.com/api/get-index) |
| [Get Site Statistics](actions/get-site-statistics.md) | `GET /stats/` | [docs](https://docs.xenforo.com/api/get-stats) |
| [Get Thread](actions/get-thread.md) | `GET /threads/:id/` | [docs](https://docs.xenforo.com/api/get-threads-id) |
| [Get Thread Posts](actions/get-thread-posts.md) | `GET /threads/:id/posts` | [docs](https://docs.xenforo.com/api/get-threads-id-posts) |
| [Get Threads](actions/get-threads.md) | `GET /threads/` | [docs](https://docs.xenforo.com/api/get-threads) |
| [Get User](actions/get-user.md) | `GET /users/:id/` | [docs](https://docs.xenforo.com/api/get-users-id) |
| [Get Users](actions/get-users.md) | `GET /users/` | [docs](https://docs.xenforo.com/api/get-users) |
| [Mark Alert](actions/mark-alert.md) | `POST /alerts/:id/mark` | [docs](https://docs.xenforo.com/api/post-alerts-id-mark) |
| [Mark Forum Read](actions/mark-forum-read.md) | `POST /forums/:id/mark-read` | [docs](https://docs.xenforo.com/api/post-forums-id-mark-read) |
| [React To Post](actions/react-to-post.md) | `POST /posts/:id/react` | [docs](https://docs.xenforo.com/api/post-posts-id-react) |
| [Send Alert](actions/send-alert.md) | `POST /alerts/` | [docs](https://docs.xenforo.com/api/post-alerts) |
| [Update Post](actions/update-post.md) | `POST /posts/:id/` | [docs](https://docs.xenforo.com/api/post-posts-id) |
| [Update Thread](actions/update-thread.md) | `POST /threads/:id/` | [docs](https://docs.xenforo.com/api/post-threads-id) |
