# Abstract Holidays: Native API Reference

A consolidated summary of Abstract Holidays's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.abstractapi.com/api/holidays
- **API base URL:** `https://holidays.abstractapi.com`

## Authentication

### API Key

Authenticate requests to Abstract Public Holidays with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.abstractapi.com/api/holidays)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Holidays](actions/get-holidays.md) | `GET /v1/` | [docs](https://docs.abstractapi.com/api/holidays) |
