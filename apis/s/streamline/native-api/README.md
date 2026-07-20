# Streamline: Native API Reference

A consolidated summary of Streamline's API configuration, with links to official documentation.

- **Official docs:** https://streamline-api.readme.io/reference/introduction
- **API base URL:** `https://public-api.streamlinehq.com`

## Authentication

### API Key

Authenticate Streamline public API requests with the x-api-key header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://streamline-api.readme.io/reference/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.
