# Dev.to: Native API Reference

A consolidated summary of Dev.to's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.forem.com/api/v1
- **OpenAPI specification:** https://developers.forem.com/redocusaurus/plugin-redoc-1.yaml
- **API base URL:** `https://dev.to/api`

## Authentication

### API key

Use a DEV API key in the api-key request header. Some public endpoints work without authentication, but user-specific and write actions require a key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://developers.forem.com/api/v1)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.forem.api-v1+json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 30; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Reaction](actions/create-reaction.md) | `POST /reactions` | [docs](https://developers.forem.com/api/v1#tag/reactions/paths/~1reactions/post) |
| [Get Article](actions/get-article.md) | `GET /articles/:id` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getArticleById) |
| [Get Article By Path](actions/get-article-by-path.md) | `GET /articles/:username/:slug` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getArticleByPath) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /users/me` | [docs](https://developers.forem.com/api/v1#tag/users/operation/getUserMe) |
| [Get Comment](actions/get-comment.md) | `GET /comments/:id` | [docs](https://developers.forem.com/api/v1#tag/comments/operation/getCommentById) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:username` | [docs](https://developers.forem.com/api/v1#tag/organizations/operation/getOrganization) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.forem.com/api/v1#tag/users/operation/getUser) |
| [List All My Articles](actions/list-all-my-articles.md) | `GET /articles/me/all` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getUserAllArticles) |
| [List Article Comments](actions/list-article-comments.md) | `GET /comments` | [docs](https://developers.forem.com/api/v1#tag/comments/operation/getCommentsByArticleId) |
| [List Followed Tags](actions/list-followed-tags.md) | `GET /follows/tags` | [docs](https://developers.forem.com/api/v1#tag/followed_tags/operation/getFollowedTags) |
| [List Followers](actions/list-followers.md) | `GET /followers/users` | [docs](https://developers.forem.com/api/v1#tag/followers/operation/getFollowers) |
| [List Latest Articles](actions/list-latest-articles.md) | `GET /articles/latest` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getLatestArticles) |
| [List My Articles](actions/list-my-articles.md) | `GET /articles/me` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getUserArticles) |
| [List My Draft Articles](actions/list-my-draft-articles.md) | `GET /articles/me/unpublished` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getUserUnpublishedArticles) |
| [List My Published Articles](actions/list-my-published-articles.md) | `GET /articles/me/published` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getUserPublishedArticles) |
| [List Organization Articles](actions/list-organization-articles.md) | `GET /organizations/:username/articles` | [docs](https://developers.forem.com/api/v1#tag/organizations/operation/getOrgArticles) |
| [List Organization Users](actions/list-organization-users.md) | `GET /organizations/:username/users` | [docs](https://developers.forem.com/api/v1#tag/organizations/operation/getOrgUsers) |
| [List Published Articles](actions/list-published-articles.md) | `GET /articles` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/getArticles) |
| [List Reading List](actions/list-reading-list.md) | `GET /readinglist` | [docs](https://developers.forem.com/api/v1#tag/readinglist/operation/getReadinglist) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developers.forem.com/api/v1#tag/tags/operation/getTags) |
| [Publish Article](actions/publish-article.md) | `POST /articles` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/createArticle) |
| [Toggle Reaction](actions/toggle-reaction.md) | `POST /reactions/toggle` | [docs](https://developers.forem.com/api/v1#tag/reactions/paths/~1reactions~1toggle/post) |
| [Unpublish Article](actions/unpublish-article.md) | `PUT /articles/:id/unpublish` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/unpublishArticle) |
| [Update Article](actions/update-article.md) | `PUT /articles/:id` | [docs](https://developers.forem.com/api/v1#tag/articles/operation/updateArticle) |
