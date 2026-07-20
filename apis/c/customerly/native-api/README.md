# Customerly: Native API Reference

A consolidated summary of Customerly's API configuration, with links to official documentation.

- **Official docs:** https://docs.customerly.io/en/api
- **API base URL:** `https://api.customerly.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authentication: <apiKey>
```

[Official authentication documentation](https://docs.customerly.io/en/articles/15223-how-to-obtain-your-api-access-token-in-customerly)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 50). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
