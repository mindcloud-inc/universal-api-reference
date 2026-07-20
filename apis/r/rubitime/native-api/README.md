# Rubitime: Native API Reference

A consolidated summary of Rubitime's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://rubitime.ru/faq/api
- **API base URL:** `https://rubitime.ru/api2`

## Authentication

### API Key

Rubitime API key generated in settings step 5, then sent as the `rk` field in JSON POST request bodies.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://rubitime.ru/faq/api)

## API conventions

Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 5000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | `POST /create-record` | [docs](https://rubitime.ru/faq/api) |
| [Get Record](actions/get-record.md) | `POST /get-record` | [docs](https://rubitime.ru/faq/api) |
| [Get Schedule](actions/get-schedule.md) | `POST /get-schedule` | [docs](https://rubitime.ru/faq/api) |
| [Remove Record](actions/remove-record.md) | `POST /remove-record` | [docs](https://rubitime.ru/faq/api) |
| [Update Record](actions/update-record.md) | `POST /update-record` | [docs](https://rubitime.ru/faq/api) |
