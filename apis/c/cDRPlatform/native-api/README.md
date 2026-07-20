# CDR Platform: Native API Reference

A consolidated summary of CDR Platform's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://cdrplatform.com/docs/open-api-schema
- **OpenAPI specification:** https://api.cdrplatform.com/schema/?format=json
- **API base URL:** `https://api.cdrplatform.com`

## Authentication

### API Key

Authenticate with a CDR Platform organisation API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://cdrplatform.com/docs/authentication-and-security)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate CO2 Removal Price](actions/calculate-co2-removal-price.md) | `POST /v1/cdr/price/` | [docs](https://api.cdrplatform.com/schema/redoc/#tag/CO2-Removal/operation/cdr_price) |
| [Get CDR Certificate By ID](actions/get-cdr-certificate-by-id.md) | `GET /v1/certificate/:id/` | [docs](https://api.cdrplatform.com/schema/redoc/#tag/Certificate/operation/certificate_retrieve_id) |
| [Purchase CO2 Removal](actions/purchase-co2-removal.md) | `POST /v1/cdr/` | [docs](https://api.cdrplatform.com/schema/redoc/#tag/CO2-Removal/operation/cdr_purchase) |
