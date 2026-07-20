# Roborabbit: Native API Reference

A consolidated summary of Roborabbit's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://developers.roborabbit.com
- **API base URL:** `https://api.roborabbit.com`

## Authentication

### API Key

Connect with a Roborabbit workspace API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.roborabbit.com/help/articles/345-where-do-i-get-my-api-key/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authorize](actions/authorize.md) | `GET /v1/auth` | [docs](https://developers.roborabbit.com/) |
| [Create Run](actions/create-run.md) | `POST /v1/tasks/:task_uid/runs` | [docs](https://developers.roborabbit.com/) |
| [Get Account](actions/get-account.md) | `GET /v1/account` | [docs](https://developers.roborabbit.com/) |
| [List Feeds](actions/list-feeds.md) | `GET /v1/feeds` | [docs](https://developers.roborabbit.com/) |
| [List Runs](actions/list-runs.md) | `GET /v1/tasks/:task_uid/runs` | [docs](https://developers.roborabbit.com/) |
| [List Tasks](actions/list-tasks.md) | `GET /v1/tasks` | [docs](https://developers.roborabbit.com/) |
| [Retrieve Run](actions/retrieve-run.md) | `GET /v1/tasks/:task_uid/runs/:uid` | [docs](https://developers.roborabbit.com/) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /v1/tasks/:uid` | [docs](https://developers.roborabbit.com/) |
