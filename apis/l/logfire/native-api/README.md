# Logfire: Native API Reference

A consolidated summary of Logfire's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://pydantic.dev/docs/logfire/manage/query-api/
- **API base URL:** `https://logfire-api.pydantic.dev`

## Authentication

### Read Token

Create a Logfire read token for the target project, then use it as the app connection API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pydantic.dev/docs/logfire/manage/query-api/)

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Exceptions](actions/list-exceptions.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [List Metrics](actions/list-metrics.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [List Recent Logs](actions/list-recent-logs.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [List Recent Records](actions/list-recent-records.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [List Recent Spans](actions/list-recent-spans.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [List Warnings And Errors](actions/list-warnings-and-errors.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/observe/explore/) |
| [Run Query](actions/run-query.md) | `GET /v1/query` | [docs](https://pydantic.dev/docs/logfire/manage/query-api/) |
