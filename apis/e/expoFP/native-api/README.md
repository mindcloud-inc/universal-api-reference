# ExpoFP: Native API Reference

A consolidated summary of ExpoFP's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://developer.expofp.com/guide/json-api
- **API base URL:** `https://app.expofp.com/api/v1`

## Authentication

### API Key

Use an ExpoFP API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.expofp.com/guide/json-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List All Expos](actions/list-all-expos.md) | `POST /list-events` | [docs](https://developer.expofp.com/guide/json-api) |
