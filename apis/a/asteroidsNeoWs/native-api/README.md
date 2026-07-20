# Asteroids NeoWs: Native API Reference

A consolidated summary of Asteroids NeoWs's API configuration, with links to official documentation.

- **Official docs:** https://api.nasa.gov/
- **API base URL:** `https://api.nasa.gov/neo/rest/v1`

## Authentication

### NASA API Key

NASA API key for api.nasa.gov expanded usage. NeoWs expects the key in the shared api_key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.nasa.gov/)

## API conventions

The total page count is read from `page.total_pages`. The current page number is read from `page.number`.

## Pagination

Use `size` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.
