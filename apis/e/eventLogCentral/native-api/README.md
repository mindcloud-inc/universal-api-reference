# EventLogCentral: Native API Reference

A consolidated summary of EventLogCentral's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.eventlogcentral.com/resources
- **API base URL:** `https://api.eventlogcentral.com`

## Authentication

### Access Token

Use your EventLogCentral access token.

### Credentials

- **Access Token:** `access_token` · required

[Official authentication documentation](https://www.eventlogcentral.com/resources/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Log Event](actions/log-event.md) | `POST /api/logEvent` | [docs](https://www.eventlogcentral.com/resources/api-documentation) |
