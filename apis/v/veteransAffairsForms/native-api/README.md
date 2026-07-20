# Veterans Affairs Forms: Native API Reference

A consolidated summary of Veterans Affairs Forms's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://developer.va.gov/explore/api/va-forms/docs
- **OpenAPI specification:** https://api.va.gov/internal/docs/forms/v0/openapi.json
- **API base URL:** `https://sandbox-api.va.gov/services/va_forms/v0`

## Authentication

### API Key

VA Forms API requests require an API key sent in the `apikey` HTTP header.

### Credentials

- **VA API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.va.gov/explore/api/va-forms/docs)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get VA Form](actions/get-va-form.md) | `GET /forms/:form_name` | [docs](https://developer.va.gov/explore/api/va-forms/docs) |
| [List VA Forms](actions/list-va-forms.md) | `GET /forms` | [docs](https://developer.va.gov/explore/api/va-forms/docs) |
