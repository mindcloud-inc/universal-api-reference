# Calendarific: Native API Reference

A consolidated summary of Calendarific's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://calendarific.com/api-documentation
- **API base URL:** `https://calendarific.com/api/v2`

## Authentication

### API Key

Authenticate Calendarific requests with an API key query parameter named api_key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://calendarific.com/api-documentation)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | `GET /countries` | [docs](https://calendarific.com/api-documentation) |
| [List Holidays](actions/list-holidays.md) | `GET /holidays` | [docs](https://calendarific.com/api-documentation) |
| [List Languages](actions/list-languages.md) | `GET /languages` | [docs](https://calendarific.com/api-documentation) |
