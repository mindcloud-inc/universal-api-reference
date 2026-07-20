# Snitcher: Native API Reference

A consolidated summary of Snitcher's API configuration, with links to official documentation.

- **Official docs:** https://docs.snitcher.com/product/rest-api/introduction
- **API base URL:** `https://api.snitcher.com/v1`

## Authentication

### Personal Access Token

Connect Snitcher with a personal access token used as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.snitcher.com/product/rest-api/introduction)

## API conventions

Response data is read from `data`. The total page count is read from `last_page`. The current page number is read from `current_page`.

## Pagination

Use `size` in the query string to set the page size (accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Multiply the delay by 2 after each failed attempt.
