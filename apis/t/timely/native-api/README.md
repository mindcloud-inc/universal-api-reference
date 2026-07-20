# Timely: Native API Reference

A consolidated summary of Timely's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.timely.com/
- **API base URL:** `https://api.timelyapp.com`

## Authentication

### OAuth 2.0

Connect Timely with OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.timelyapp.com/1.1/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.timelyapp.com/1.1/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `manage`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.timelyapp.com/1.1/oauth/token.

[Official authentication documentation](https://developer.timely.com/)

## Pagination

Use `per_page` in the query string to set the page size (default 100; accepted range 1–5000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Import Time Entries](actions/bulk-import-time-entries.md) | `POST /1.1/{account_id}/bulk/hours` | [docs](https://developer.timely.com/) |
| [Create Client](actions/create-client.md) | `POST /1.1/{account_id}/clients` | [docs](https://developer.timely.com/) |
| [Create Project](actions/create-project.md) | `POST /1.1/{account_id}/projects` | [docs](https://developer.timely.com/) |
| [Create Tag](actions/create-tag.md) | `POST /1.1/{account_id}/labels` | [docs](https://developer.timely.com/) |
| [Create Task](actions/create-task.md) | `POST /1.1/{account_id}/forecasts` | [docs](https://developer.timely.com/) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /1.1/{account_id}/hours` | [docs](https://developer.timely.com/) |
| [Create Webhook](actions/create-webhook.md) | `POST /1.1/{account_id}/webhooks` | [docs](https://developer.timely.com/) |
| [Delete Project](actions/delete-project.md) | `DELETE /1.1/{account_id}/projects/{id}` | [docs](https://developer.timely.com/) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /1.1/{account_id}/labels/{id}` | [docs](https://developer.timely.com/) |
| [Delete Task](actions/delete-task.md) | `DELETE /1.1/{account_id}/forecasts/{id}` | [docs](https://developer.timely.com/) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /1.1/{account_id}/hours/{id}` | [docs](https://developer.timely.com/) |
| [Filter Reports](actions/filter-reports.md) | `GET /1.1/{account_id}/reports/filter` | [docs](https://developer.timely.com/) |
| [Get Client](actions/get-client.md) | `GET /1.1/{account_id}/clients/{id}` | [docs](https://developer.timely.com/) |
| [Get Current Token Info](actions/get-current-token-info.md) | `GET /1.1/oauth/token/info` | [docs](https://developer.timely.com/) |
| [Get Current User](actions/get-current-user.md) | `GET /1.1/{account_id}/users/current` | [docs](https://developer.timely.com/) |
| [Get Project](actions/get-project.md) | `GET /1.1/{account_id}/projects/{id}` | [docs](https://developer.timely.com/) |
| [Get Report Totals](actions/get-report-totals.md) | `GET /1.1/{account_id}/reports` | [docs](https://developer.timely.com/) |
| [Get Tag](actions/get-tag.md) | `GET /1.1/{account_id}/labels/{id}` | [docs](https://developer.timely.com/) |
| [Get Task](actions/get-task.md) | `GET /1.1/{account_id}/forecasts/{id}` | [docs](https://developer.timely.com/) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /1.1/{account_id}/hours/{id}` | [docs](https://developer.timely.com/) |
| [Get User](actions/get-user.md) | `GET /1.1/{account_id}/users/{id}` | [docs](https://developer.timely.com/) |
| [Get Webhook](actions/get-webhook.md) | `GET /1.1/{account_id}/webhooks/{id}` | [docs](https://developer.timely.com/) |
| [Invite User](actions/invite-user.md) | `POST /1.1/{account_id}/users` | [docs](https://developer.timely.com/) |
| [List Clients](actions/list-clients.md) | `GET /1.1/{account_id}/clients` | [docs](https://developer.timely.com/) |
| [List Projects](actions/list-projects.md) | `GET /1.1/{account_id}/projects` | [docs](https://developer.timely.com/) |
| [List Tags](actions/list-tags.md) | `GET /1.1/{account_id}/labels` | [docs](https://developer.timely.com/) |
| [List Task Summaries](actions/list-task-summaries.md) | `GET /1.1/{account_id}/forecasts/{resource}/summary` | [docs](https://developer.timely.com/) |
| [List Tasks](actions/list-tasks.md) | `GET /1.1/{account_id}/forecasts` | [docs](https://developer.timely.com/) |
| [List Time Entries](actions/list-time-entries.md) | `GET /1.1/{account_id}/hours` | [docs](https://developer.timely.com/) |
| [List Users](actions/list-users.md) | `GET /1.1/{account_id}/users` | [docs](https://developer.timely.com/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /1.1/{account_id}/webhooks` | [docs](https://developer.timely.com/) |
| [Search Users](actions/search-users.md) | `GET /1.1/{account_id}/users/search` | [docs](https://developer.timely.com/) |
| [Start Time Entry Timer](actions/start-time-entry-timer.md) | `PUT /1.1/{account_id}/hours/{id}/start` | [docs](https://developer.timely.com/) |
| [Stop Time Entry Timer](actions/stop-time-entry-timer.md) | `PUT /1.1/{account_id}/hours/{id}/stop` | [docs](https://developer.timely.com/) |
| [Update Client](actions/update-client.md) | `PUT /1.1/{account_id}/clients/{id}` | [docs](https://developer.timely.com/) |
| [Update Project](actions/update-project.md) | `PUT /1.1/{account_id}/projects/{id}` | [docs](https://developer.timely.com/) |
| [Update Tag](actions/update-tag.md) | `PUT /1.1/{account_id}/labels/{id}` | [docs](https://developer.timely.com/) |
| [Update Task](actions/update-task.md) | `PATCH /1.1/{account_id}/forecasts/{id}` | [docs](https://developer.timely.com/) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /1.1/{account_id}/hours/{id}` | [docs](https://developer.timely.com/) |
| [Update User](actions/update-user.md) | `PUT /1.1/{account_id}/users/{id}` | [docs](https://developer.timely.com/) |
