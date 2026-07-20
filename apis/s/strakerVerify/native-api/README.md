# Straker Verify: Native API Reference

A consolidated summary of Straker Verify's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://api-verify.straker.ai/docs
- **OpenAPI specification:** https://api-verify.straker.ai/openapi.json
- **API base URL:** `https://api-verify.straker.ai`

## Authentication

### API Key

Use a Straker Verify API key for bearer authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.straker.ai/en/docs/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Token Balance](actions/get-token-balance.md) | `GET /user/balance` | [docs](https://api-verify.straker.ai/docs#/default/get_token_balance_user_balance_get) |
