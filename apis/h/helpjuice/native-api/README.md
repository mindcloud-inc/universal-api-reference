# Helpjuice: Native API Reference

A consolidated summary of Helpjuice's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://help.helpjuice.com/using-api-v3
- **API base URL:** `{baseUrl}`

## Authentication

### Helpjuice API Key

Authenticate to Helpjuice with an account-specific API base URL and API key.

### Credentials

- **Base URL:** `baseUrl` · required · Your Helpjuice API base URL, for example https://mindcloud.helpjuice.com/api/v3.
- **API Key:** `apiKey` · required · Your Helpjuice private API key from Settings > API Credentials.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.helpjuice.com/api-v3-webhooks/284079-how-do-i-get-my-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate User](actions/activate-user.md) | `PUT /users/:id/activate` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Create Article](actions/create-article.md) | `POST /articles` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Deactivate User](actions/deactivate-user.md) | `PUT /users/:id/deactivate` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Delete Article](actions/delete-article.md) | `DELETE /articles/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Downvote Article](actions/downvote-article.md) | `PUT /articles/:id/downvote` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Account Settings](actions/get-account-settings.md) | `GET /settings/account` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Activity](actions/get-activity.md) | `GET /activities/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Article](actions/get-article.md) | `GET /articles/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Category](actions/get-category.md) | `GET /categories/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Article Analytics](actions/list-article-analytics.md) | `GET /analytics/questions` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Articles](actions/list-articles.md) | `GET /articles` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Backups](actions/list-backups.md) | `GET /backups` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Category Analytics](actions/list-category-analytics.md) | `GET /analytics/categories` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Group Analytics](actions/list-group-analytics.md) | `GET /analytics/groups` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Group Users](actions/list-group-users.md) | `GET /groups/:id/users` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Search Analytics](actions/list-search-analytics.md) | `GET /analytics/searches` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List User Analytics](actions/list-user-analytics.md) | `GET /analytics/users` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Search KB](actions/search-kb.md) | `GET /search` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Test Webhook](actions/test-webhook.md) | `POST /webhooks/:id/test` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Toggle Webhook](actions/toggle-webhook.md) | `PUT /webhooks/:id/toggle` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Update Article](actions/update-article.md) | `PUT /articles/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Update Category](actions/update-category.md) | `PUT /categories/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Update User](actions/update-user.md) | `PUT /users/:id` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
| [Upvote Article](actions/upvote-article.md) | `PUT /articles/:id/upvote` | [docs](https://help.helpjuice.com/api-v3/using-api-v3) |
