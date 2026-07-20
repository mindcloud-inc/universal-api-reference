# LOBSTR.IO: Native API Reference

A consolidated summary of LOBSTR.IO's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.lobstr.io
- **API base URL:** `https://api.lobstr.io`

## Authentication

### API Key

Authenticate with your Lobstr.io API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.lobstr.io/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; maximum 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tasks](actions/add-tasks.md) | `POST /v1/tasks` | [docs](https://docs.lobstr.io/docs/add-tasks) |
| [Check Sync Status](actions/check-sync-status.md) | `GET /v1/synchronize/:sync_task_id` | [docs](https://docs.lobstr.io/docs/check-sync-status) |
| [Check Upload Status](actions/check-upload-status.md) | `GET /v1/tasks/upload/:upload_task_id` | [docs](https://docs.lobstr.io/docs/check-upload-status) |
| [Create Squid](actions/create-squid.md) | `POST /v1/squids` | [docs](https://docs.lobstr.io/docs/create-squid) |
| [Delete Squid](actions/delete-squid.md) | `DELETE /v1/squids/:squid_hash` | [docs](https://docs.lobstr.io/docs/delete-squid) |
| [Get Account Details](actions/get-account-details.md) | `GET /v1/accounts/:account_hash` | [docs](https://docs.lobstr.io/docs/get-account-details) |
| [Get Crawler Attributes](actions/get-crawler-attributes.md) | `GET /v1/crawlers/:crawler_hash/attributes` | [docs](https://docs.lobstr.io/docs/get-crawler-attributes) |
| [Get Crawler Details](actions/get-crawler-details.md) | `GET /v1/crawlers/:crawler_hash` | [docs](https://docs.lobstr.io/docs/get-crawler-details) |
| [Get Crawler Parameters](actions/get-crawler-parameters.md) | `GET /v1/crawlers/:crawler_hash/params` | [docs](https://docs.lobstr.io/docs/get-crawler-parameters) |
| [Get Results](actions/get-results.md) | `GET /v1/results` | [docs](https://docs.lobstr.io/docs/get-results) |
| [Get Run](actions/get-run.md) | `GET /v1/runs/:run_hash` | [docs](https://docs.lobstr.io/docs/get-run) |
| [Get Run Stats](actions/get-run-stats.md) | `GET /v1/runs/:run_hash/stats` | [docs](https://docs.lobstr.io/docs/get-run-stats) |
| [Get Squid Details](actions/get-squid-details.md) | `GET /v1/squids/:squid_hash` | [docs](https://docs.lobstr.io/docs/get-squid-details) |
| [Get User Profile](actions/get-user-profile.md) | `GET /v1/me` | [docs](https://docs.lobstr.io/docs/user-me) |
| [List Accounts](actions/list-accounts.md) | `GET /v1/accounts` | [docs](https://docs.lobstr.io/docs/list-accounts) |
| [List Crawlers](actions/list-crawlers.md) | `GET /v1/crawlers` | [docs](https://docs.lobstr.io/docs/list-crawlers) |
| [List Runs](actions/list-runs.md) | `GET /v1/runs` | [docs](https://docs.lobstr.io/docs/list-runs) |
| [List Squids](actions/list-squids.md) | `GET /v1/squids` | [docs](https://docs.lobstr.io/docs/list-squids) |
| [List Tasks](actions/list-tasks.md) | `GET /v1/tasks` | [docs](https://docs.lobstr.io/docs/list-tasks) |
| [Refresh Cookies](actions/refresh-cookies.md) | `POST /v1/accounts/cookies` | [docs](https://docs.lobstr.io/docs/refresh-cookies) |
| [Start Run](actions/start-run.md) | `POST /v1/runs` | [docs](https://docs.lobstr.io/docs/start-run) |
| [Sync Account](actions/sync-account.md) | `POST /v1/accounts/cookies` | [docs](https://docs.lobstr.io/docs/sync-account) |
| [Update Squid](actions/update-squid.md) | `POST /v1/squids/:squid_hash` | [docs](https://docs.lobstr.io/docs/update-squid) |
| [Upload Tasks](actions/upload-tasks.md) | `POST /v1/tasks/upload` | [docs](https://docs.lobstr.io/docs/upload-tasks) |
