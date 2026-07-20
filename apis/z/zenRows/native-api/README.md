# ZenRows: Native API Reference

A consolidated summary of ZenRows's API configuration, with links to official documentation.

- **Official docs:** https://docs.zenrows.com/first-steps/welcome
- **API base URL:** `https://api.zenrows.com/v1`

## Authentication

### API Key

Authenticate with your ZenRows API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.zenrows.com/first-steps/getting-started-guide)

## API conventions

The next-page cursor is read from `pagination.nextPage`. The total page count is read from `pagination.pageCount`. The current page number is read from `pagination.currentPage`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.
