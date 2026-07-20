# Beamer: Native API Reference

A consolidated summary of Beamer's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://help.userflow.com/beamer/docs/beamer-api-reference
- **API base URL:** `https://api.getbeamer.com`

## Authentication

### API Key

Authenticate Beamer requests with an API key generated in Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.userflow.com/beamer/docs/how-to-resolve-a-403-error-in-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `maxResults` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Post Comments](actions/count-post-comments.md) | `GET /v0/posts/:postId/comments/count` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Count Post Reactions](actions/count-post-reactions.md) | `GET /v0/posts/:postId/reactions/count` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Count Posts](actions/count-posts.md) | `GET /v0/posts/count` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Create Post](actions/create-post.md) | `POST /v0/posts` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Create Post Comment](actions/create-post-comment.md) | `POST /v0/posts/:postId/comments` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Create Post Reaction](actions/create-post-reaction.md) | `POST /v0/posts/:postId/reactions` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Delete Post](actions/delete-post.md) | `DELETE /v0/posts/:postId` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Delete Post Reaction](actions/delete-post-reaction.md) | `DELETE /v0/posts/:postId/reactions/:reactionId` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Get Feed URL](actions/get-feed-url.md) | `GET /v0/url` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Get Post By ID](actions/get-post-by-id.md) | `GET /v0/posts/:postId` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Get Post Reaction By ID](actions/get-post-reaction-by-id.md) | `GET /v0/posts/:postId/reactions/:reactionId` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Get Unread Count](actions/get-unread-count.md) | `GET /v0/unread/count` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [List Post Comments](actions/list-post-comments.md) | `GET /v0/posts/:postId/comments` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [List Post Reactions](actions/list-post-reactions.md) | `GET /v0/posts/:postId/reactions` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [List Posts](actions/list-posts.md) | `GET /v0/posts` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [List Unread Posts](actions/list-unread-posts.md) | `GET /v0/unread` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Ping API](actions/ping-api.md) | `POST /v0/ping` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
| [Update Post](actions/update-post.md) | `PUT /v0/posts/:postId` | [docs](https://help.userflow.com/beamer/docs/beamer-api-reference) |
