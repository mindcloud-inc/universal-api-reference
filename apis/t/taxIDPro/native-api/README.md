# Tax ID Pro: Native API Reference

A consolidated summary of Tax ID Pro's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://taxid.pro/docs/getting-started
- **API base URL:** `https://v3.api.taxid.pro`

## Authentication

### API Key

Authenticate Tax ID Pro API requests with an API key in the Authorization header using Bearer token format.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://taxid.pro/docs/authentication)

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

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Validate Tax IDs](actions/batch-validate-tax-ids.md) | `POST /validate` | [docs](https://taxid.pro/docs/batch-validation) |
| [Validate Tax ID](actions/validate-tax-id.md) | `GET /validate` | [docs](https://taxid.pro/docs/tax-id-validation) |
