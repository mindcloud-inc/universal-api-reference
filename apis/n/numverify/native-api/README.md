# Numverify: Native API Reference

A consolidated summary of Numverify's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.apilayer.com/numverify/docs/api-documentation
- **OpenAPI specification:** https://api.swaggerhub.com/apis/apilayer-863/numverify-api/1.0.0/swagger.json
- **API base URL:** `https://apilayer.net/api`

## Authentication

### API Key

Authenticate Numverify requests with your API access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.apilayer.com/numverify/docs/api-key-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Supported Countries](actions/list-supported-countries.md) | `GET /countries` | [docs](https://docs.apilayer.com/numverify/docs/numverify-api-v-1-0-0) |
| [Validate Phone Number](actions/validate-phone-number.md) | `GET /validate` | [docs](https://docs.apilayer.com/numverify/docs/numverify-api-v-1-0-0) |
