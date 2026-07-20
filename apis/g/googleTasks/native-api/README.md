# Google Tasks: Native API Reference

A consolidated summary of Google Tasks's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/workspace/tasks/reference/rest
- **OpenAPI specification:** https://www.googleapis.com/discovery/v1/apis/tasks/v1/rest
- **API base URL:** `https://tasks.googleapis.com/tasks/v1`

## Authentication

### OAuth 2.0

Google OAuth 2.0 for Google Tasks API

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/tasks openid https://www.googleapis.com/auth/userinfo.email https://www.googleapis.com/auth/userinfo.profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/workspace/tasks/auth)

## Pagination

Use `maxResults` in the query string to set the page size (default 20; accepted range 1–100). Use `pageToken` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | `POST /lists/:tasklist/tasks` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/insert) |
| [Delete Task](actions/delete-task.md) | `DELETE /lists/:tasklist/tasks/:task` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/delete) |
| [Get Task](actions/get-task.md) | `GET /lists/:tasklist/tasks/:task` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/get) |
| [List Task Lists](actions/list-task-lists.md) | `GET /users/@me/lists` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasklists/list) |
| [List Tasks](actions/list-tasks.md) | `GET /lists/:tasklist/tasks` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/list) |
| [Update Task](actions/update-task.md) | `PATCH /lists/:tasklist/tasks/:task` | [docs](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/patch) |
