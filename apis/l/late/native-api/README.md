# Late: Native API Reference

A consolidated summary of Late's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.zernio.com
- **OpenAPI specification:** https://docs.zernio.com/api/openapi
- **API base URL:** `https://zernio.com/api/v1`

## Authentication

### API Key

API key authentication for the Zernio API using an Authorization: Bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.zernio.com/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `pagination.pages`. The current page number is read from `pagination.page`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Accounts Health](actions/check-accounts-health.md) | `GET /accounts/health` | [docs](https://docs.zernio.com/accounts/check-accounts-health) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://docs.zernio.com/posts/create-post) |
| [Create Profile](actions/create-profile.md) | `POST /profiles` | [docs](https://docs.zernio.com/profiles/create-profile) |
| [Create Queue Schedule](actions/create-queue-schedule.md) | `POST /queue/slots` | [docs](https://docs.zernio.com/queue/create-schedule) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:postId` | [docs](https://docs.zernio.com/posts/delete-post) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /profiles/:profileId` | [docs](https://docs.zernio.com/profiles/delete-profile) |
| [Delete Queue Schedule](actions/delete-queue-schedule.md) | `DELETE /queue/slots` | [docs](https://docs.zernio.com/queue/delete-schedule) |
| [Get Next Queue Slot](actions/get-next-queue-slot.md) | `GET /queue/next-slot` | [docs](https://docs.zernio.com/queue/get-next-available-slot) |
| [Get Post](actions/get-post.md) | `GET /posts/:postId` | [docs](https://docs.zernio.com/posts/get-post) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/:profileId` | [docs](https://docs.zernio.com/profiles/get-profile) |
| [Get Usage Stats](actions/get-usage-stats.md) | `GET /usage-stats` | [docs](https://docs.zernio.com/usage/get-plan-and-usage-stats) |
| [List Account Groups](actions/list-account-groups.md) | `GET /account-groups` | [docs](https://docs.zernio.com/account-groups/list-groups) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.zernio.com/accounts/list-accounts) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://docs.zernio.com/posts/list-posts) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://docs.zernio.com/profiles/list-profiles) |
| [List Queue Schedules](actions/list-queue-schedules.md) | `GET /queue/slots` | [docs](https://docs.zernio.com/queue/list-schedules) |
| [Preview Queue Slots](actions/preview-queue-slots.md) | `GET /queue/preview` | [docs](https://docs.zernio.com/queue/preview-upcoming-slots) |
| [Update Post](actions/update-post.md) | `PUT /posts/:postId` | [docs](https://docs.zernio.com/posts/update-post) |
| [Update Profile](actions/update-profile.md) | `PUT /profiles/:profileId` | [docs](https://docs.zernio.com/profiles/update-profile) |
| [Update Queue Schedule](actions/update-queue-schedule.md) | `PUT /queue/slots` | [docs](https://docs.zernio.com/queue/update-schedule) |
