# BlogIn: Native API Reference

A consolidated summary of BlogIn's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://blogin.co/api/rest/docs/
- **API base URL:** `https://blogin.co/api/rest`

## Authentication

### API Key

Connect BlogIn with a bearer API key from Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://blogin.co/api/rest/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 10–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Use `@` for ascending order and `-` for descending order. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Post Comment](actions/add-post-comment.md) | `POST /posts/:id/comments` | [docs](https://blogin.co/api/rest/docs/#create-new-post-comment) |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://blogin.co/api/rest/docs/#create-new-category) |
| [Create Member](actions/create-member.md) | `POST /members` | [docs](https://blogin.co/api/rest/docs/#create-new-member) |
| [Create Page](actions/create-page.md) | `POST /pages` | [docs](https://blogin.co/api/rest/docs/#create-new-page) |
| [Create Post](actions/create-post.md) | `POST /posts` | [docs](https://blogin.co/api/rest/docs/#create-new-post) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:id` | [docs](https://blogin.co/api/rest/docs/#delete-a-category) |
| [Delete Member](actions/delete-member.md) | `DELETE /members/:id` | [docs](https://blogin.co/api/rest/docs/#delete-a-specific-member) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/:id` | [docs](https://blogin.co/api/rest/docs/#delete-a-page) |
| [Delete Post](actions/delete-post.md) | `DELETE /posts/:id` | [docs](https://blogin.co/api/rest/docs/#delete-a-post) |
| [Delete Post Comment](actions/delete-post-comment.md) | `DELETE /posts/:postId/comments/:commentId` | [docs](https://blogin.co/api/rest/docs/#delete-a-post-comment) |
| [Delete Team](actions/delete-team.md) | `DELETE /teams/:id` | [docs](https://blogin.co/api/rest/docs/#delete-a-team) |
| [Get Category](actions/get-category.md) | `GET /categories/:id` | [docs](https://blogin.co/api/rest/docs/#get-a-specific-category) |
| [Get Member](actions/get-member.md) | `GET /members/:id` | [docs](https://blogin.co/api/rest/docs/#get-a-specific-member) |
| [Get Page](actions/get-page.md) | `GET /pages/:id` | [docs](https://blogin.co/api/rest/docs/#get-a-specific-page) |
| [Get Post](actions/get-post.md) | `GET /posts/:id` | [docs](https://blogin.co/api/rest/docs/#get-a-specific-post) |
| [Get Team](actions/get-team.md) | `GET /teams/:id` | [docs](https://blogin.co/api/rest/docs/#get-a-specific-team) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://blogin.co/api/rest/docs/#get-all-categories) |
| [List Members](actions/list-members.md) | `GET /members` | [docs](https://blogin.co/api/rest/docs/#get-all-members) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://blogin.co/api/rest/docs/#get-all-pages) |
| [List Post Comments](actions/list-post-comments.md) | `GET /posts/:id/comments` | [docs](https://blogin.co/api/rest/docs/#get-all-post-comments) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://blogin.co/api/rest/docs/#get-all-posts) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://blogin.co/api/rest/docs/#get-all-tags) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://blogin.co/api/rest/docs/#get-all-teams) |
| [Search](actions/search.md) | `GET /search` | [docs](https://blogin.co/api/rest/docs/#search-2) |
| [Update Category](actions/update-category.md) | `POST /categories/:id` | [docs](https://blogin.co/api/rest/docs/#update-a-category) |
| [Update Member](actions/update-member.md) | `POST /members/:id` | [docs](https://blogin.co/api/rest/docs/#update-a-specific-member) |
| [Update Page](actions/update-page.md) | `POST /pages/:id` | [docs](https://blogin.co/api/rest/docs/#update-a-page) |
| [Update Post](actions/update-post.md) | `POST /posts/:id` | [docs](https://blogin.co/api/rest/docs/#update-a-post) |
| [Update Post Comment](actions/update-post-comment.md) | `POST /posts/:postId/comments/:commentId` | [docs](https://blogin.co/api/rest/docs/#update-a-post-comment) |
| [Update Team](actions/update-team.md) | `POST /teams/:id` | [docs](https://blogin.co/api/rest/docs/#update-a-team) |
