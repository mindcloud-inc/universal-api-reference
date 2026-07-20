# Festivo: Native API Reference

A consolidated summary of Festivo's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.getfestivo.com/docs/products/public-holidays-api/intro/
- **API base URL:** `https://api.getfestivo.com/v3`

## Authentication

### API Key

Authenticate Festivo API requests with the API key from the Festivo dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.getfestivo.com/docs/before-you-start)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `holidays`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Available Countries](actions/list-available-countries.md) | `GET /public-holidays/countries` | [docs](https://docs.getfestivo.com/docs/products/public-holidays-api/list-countries/) |
| [List Public Holidays](actions/list-public-holidays.md) | `GET /public-holidays/list` | [docs](https://docs.getfestivo.com/docs/products/public-holidays-api/list-holidays/) |
