# TextMagic: Native API Reference

A consolidated summary of TextMagic's API configuration, with links to official documentation.

- **Official docs:** https://docs.textmagic.com/
- **OpenAPI specification:** https://docs.textmagic.com/swagger.json
- **API base URL:** `https://rest.textmagic.com/api/v2`

## Authentication

### API Key

Authenticate with your TextMagic username and API key.

### Credentials

- **API Key:** `apiKey` · required
- **Username:** `username` · required · Your TextMagic username.

Send these headers with each API request:

```http
X-TM-Key: <apiKey>
X-TM-Username: <username>
```

[Official authentication documentation](https://docs.textmagic.com/#section/Getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
