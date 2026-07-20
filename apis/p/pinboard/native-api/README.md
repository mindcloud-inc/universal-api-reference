# Pinboard: Native API Reference

A consolidated summary of Pinboard's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://pinboard.in/api/
- **API base URL:** `https://api.pinboard.in/v1`

## Authentication

### API Token

Connect with your Pinboard username and API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pinboard.in/api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Bookmark](actions/add-bookmark.md) | `GET /posts/add` | [docs](https://pinboard.in/api/#posts_add) |
| [Delete Bookmark](actions/delete-bookmark.md) | `GET /posts/delete` | [docs](https://pinboard.in/api/#posts_delete) |
| [Delete Tag](actions/delete-tag.md) | `GET /tags/delete` | [docs](https://pinboard.in/api/#tags_delete) |
| [Get Latest Bookmark Update](actions/get-latest-bookmark-update.md) | `GET /posts/update` | [docs](https://pinboard.in/api/#posts_update) |
| [Get Note](actions/get-note.md) | `GET /notes/:id` | [docs](https://pinboard.in/api/#notes_get) |
| [Get User API Token](actions/get-user-api-token.md) | `GET /user/api_token` | [docs](https://pinboard.in/api/#user_api_token) |
| [Get User Secret](actions/get-user-secret.md) | `GET /user/secret` | [docs](https://pinboard.in/api/#user_secret) |
| [List All Posts](actions/list-all-posts.md) | `GET /posts/all` | [docs](https://pinboard.in/api/#posts_all) |
| [List Notes](actions/list-notes.md) | `GET /notes/list` | [docs](https://pinboard.in/api/#notes_list) |
| [List Post Dates](actions/list-post-dates.md) | `GET /posts/dates` | [docs](https://pinboard.in/api/#posts_dates) |
| [List Posts](actions/list-posts.md) | `GET /posts/get` | [docs](https://pinboard.in/api/#posts_get) |
| [List Recent Posts](actions/list-recent-posts.md) | `GET /posts/recent` | [docs](https://pinboard.in/api/#posts_recent) |
| [List Tags](actions/list-tags.md) | `GET /tags/get` | [docs](https://pinboard.in/api/#tags_get) |
| [Suggest Tags For URL](actions/suggest-tags-for-url.md) | `GET /posts/suggest` | [docs](https://pinboard.in/api/#posts_suggest) |
