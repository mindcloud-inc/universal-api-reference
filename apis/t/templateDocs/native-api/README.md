# TemplateDocs: Native API Reference

A consolidated summary of TemplateDocs's API configuration, with links to official documentation.

- **Official docs:** https://templatedocs.io/docs/api/overview
- **API base URL:** `https://templatedocs.io/api`

## Authentication

### API Key

Authenticate with your TemplateDocs API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://templatedocs.io/docs/api/auth)

## API conventions

Response data is read from `templates`.

## Pagination

Use `pageIndex` in the query string to choose the page; numbering starts at 1.
