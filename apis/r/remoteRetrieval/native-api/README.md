# Remote Retrieval: Native API Reference

A consolidated summary of Remote Retrieval's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://www.remoteretrieval.com/api-integration
- **API base URL:** `https://www.remoteretrieval.com`

## Authentication

### API Key

Authenticate to the Remote Retrieval API with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.remoteretrieval.com/api-integration)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Details](actions/get-company-details.md) | `GET /api/v1/company-details` | [docs](https://www.remoteretrieval.com/api-integration) |
| [Get Device Prices](actions/get-device-prices.md) | `GET /api/v1/get-device-prices` | [docs](https://www.remoteretrieval.com/api-integration) |
| [Validate User](actions/validate-user.md) | `GET /api/v1/validate/user` | [docs](https://www.remoteretrieval.com/api-integration) |
