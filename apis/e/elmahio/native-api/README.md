# elmah.io: Native API Reference

A consolidated summary of elmah.io's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.elmah.io/using-the-rest-api/
- **OpenAPI specification:** https://api.elmah.io/swagger/docs/v3
- **API base URL:** `https://api.elmah.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.elmah.io/how-to-configure-api-key-permissions/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | `POST /v3/deployments` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Create Heartbeat](actions/create-heartbeat.md) | `POST /v3/heartbeats/:logId/:id` | [docs](https://api.elmah.io/swagger/index.html) |
| [Create Log](actions/create-log.md) | `POST /v3/logs` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Create Message](actions/create-message.md) | `POST /v3/messages/:logId` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Create Messages Bulk](actions/create-messages-bulk.md) | `POST /v3/messages/:logId/_bulk` | [docs](https://api.elmah.io/swagger/index.html) |
| [Delete Deployment](actions/delete-deployment.md) | `DELETE /v3/deployments/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Delete Log](actions/delete-log.md) | `DELETE /v3/logs/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Delete Message](actions/delete-message.md) | `DELETE /v3/messages/:logId/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Delete Messages](actions/delete-messages.md) | `DELETE /v3/messages/:logId` | [docs](https://api.elmah.io/swagger/index.html) |
| [Diagnose Log](actions/diagnose-log.md) | `GET /v3/logs/:id/_diagnose` | [docs](https://api.elmah.io/swagger/index.html) |
| [Disable Log](actions/disable-log.md) | `POST /v3/logs/:id/_disable` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Enable Log](actions/enable-log.md) | `POST /v3/logs/:id/_enable` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Fix Message](actions/fix-message.md) | `POST /v3/messages/:logId/:id/_fix` | [docs](https://api.elmah.io/swagger/index.html) |
| [Fix Messages](actions/fix-messages.md) | `POST /v3/messages/:logId/_fix` | [docs](https://api.elmah.io/swagger/index.html) |
| [Get Deployment](actions/get-deployment.md) | `GET /v3/deployments/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Get Log](actions/get-log.md) | `GET /v3/logs/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Get Message](actions/get-message.md) | `GET /v3/messages/:logId/:id` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [Hide Message](actions/hide-message.md) | `POST /v3/messages/:logId/:id/_hide` | [docs](https://api.elmah.io/swagger/index.html) |
| [List Deployments](actions/list-deployments.md) | `GET /v3/deployments` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [List Logs](actions/list-logs.md) | `GET /v3/logs` | [docs](https://docs.elmah.io/using-the-rest-api/) |
| [List Messages](actions/list-messages.md) | `GET /v3/messages/:logId` | [docs](https://docs.elmah.io/using-the-rest-api/) |
