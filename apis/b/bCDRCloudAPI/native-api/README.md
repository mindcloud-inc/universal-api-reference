# BCDR Cloud: Native API Reference

A consolidated summary of BCDR Cloud's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://support.bdrshield.com/portal/en/kb/articles/api-management-execution
- **API base URL:** `https://console1.bdrshield.com/api/v1`

## Authentication

### Bearer Token

Authenticate with a BDRShield cloud session bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.bdrshield.com/portal/en/kb/articles/api-management-execution)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Config Values](actions/get-config-values.md) | `POST /getconfigvalue` | [docs](https://console1.bdrshield.com/v/#/newdashboard) |
| [Get Notifications Count](actions/get-notifications-count.md) | `POST /getnotificationscount` | [docs](https://console1.bdrshield.com/v/#/newdashboard) |
| [Get Portal Server](actions/get-portal-server.md) | `POST /portal_server` | [docs](https://console1.bdrshield.com/v/#/infrastructure/backup/endpoint) |
| [Get Product Labels](actions/get-product-labels.md) | `POST /get_prod_labels` | [docs](https://console1.bdrshield.com/v/#/newdashboard) |
