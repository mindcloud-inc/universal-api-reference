# Walls.io: Native API Reference

A consolidated summary of Walls.io's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://github.com/DieSocialisten/Walls.io-API-Docs
- **API base URL:** `https://api.walls.io/v1`

## Authentication

### Access Token

Use the built-in API Key field to paste your Walls.io access token. MindCloud reuses that single secret as the Bearer token header value and as the access_token query parameter required by Walls.io.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://walls.io/api-info)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clear Post Spam](actions/clear-post-spam.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
| [Create Hidden Post](actions/create-hidden-post.md) | `POST /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md) |
| [Create Image Post](actions/create-image-post.md) | `POST /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md) |
| [Create Pinned Post](actions/create-pinned-post.md) | `POST /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md) |
| [Create Scheduled Post](actions/create-scheduled-post.md) | `POST /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md) |
| [Create Text Post](actions/create-text-post.md) | `POST /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/POST_posts.md) |
| [Get Post](actions/get-post.md) | `GET /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-postid.md) |
| [Get Post Analytics](actions/get-post-analytics.md) | `GET /analytics/posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_analytics-posts.md) |
| [Get Post Analytics By Type](actions/get-post-analytics-by-type.md) | `GET /analytics/posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_analytics-posts.md) |
| [Get Post With Source](actions/get-post-with-source.md) | `GET /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-postid.md) |
| [Get User Analytics](actions/get-user-analytics.md) | `GET /analytics/users` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_analytics-users.md) |
| [Get User Analytics By Type](actions/get-user-analytics-by-type.md) | `GET /analytics/users` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_analytics-users.md) |
| [List Ads](actions/list-ads.md) | `GET /ads` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_ads.md) |
| [List Changed Pinned Posts](actions/list-changed-pinned-posts.md) | `GET /posts/changed` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md) |
| [List Changed Posts](actions/list-changed-posts.md) | `GET /posts/changed` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md) |
| [List Changed Posts By Language](actions/list-changed-posts-by-language.md) | `GET /posts/changed` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md) |
| [List Changed Posts By Media Type](actions/list-changed-posts-by-media-type.md) | `GET /posts/changed` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md) |
| [List Changed Posts By Type](actions/list-changed-posts-by-type.md) | `GET /posts/changed` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts-changed.md) |
| [List Pinned Posts](actions/list-pinned-posts.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts After ID](actions/list-posts-after-id.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts Before ID](actions/list-posts-before-id.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts By Language](actions/list-posts-by-language.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts By Media Type](actions/list-posts-by-media-type.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts By Type](actions/list-posts-by-type.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [List Posts With Source](actions/list-posts-with-source.md) | `GET /posts` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/GET_posts.md) |
| [Pin Post](actions/pin-post.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
| [Report Post Spam](actions/report-post-spam.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
| [Unpin Post](actions/unpin-post.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
| [Update Post Language](actions/update-post-language.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
| [Update Post Visibility](actions/update-post-visibility.md) | `PUT /posts/:postId` | [docs](https://github.com/DieSocialisten/Walls.io-API-Docs/blob/master/endpoints/PUT_posts-postid.md) |
