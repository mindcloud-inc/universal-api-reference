# Abstract IBAN Validator: Native API Reference

A consolidated summary of Abstract IBAN Validator's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.abstractapi.com/api/iban-validation
- **API base URL:** `https://ibanvalidation.abstractapi.com`

## Authentication

### API Key

Authenticate requests to Abstract IBAN Validation with the API key for this specific Abstract API product.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.abstractapi.com/api/iban-validation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Validate IBAN](actions/validate-iban.md) | `GET /v1/` | [docs](https://docs.abstractapi.com/api/iban-validation) |
