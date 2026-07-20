# Courier: Native API Reference

A consolidated summary of Courier's API configuration, with links to official documentation.

- **Official docs:** https://www.courier.com/docs/reference
- **API base URL:** `https://api.courier.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.courier.com/docs/reference/get-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `paging.cursor`.

## Pagination

Use `cursor` in the query string as the pagination cursor.
