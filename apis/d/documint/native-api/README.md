# Documint: Native API Reference

A consolidated summary of Documint's API configuration and 5 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/11741160/TVK5cLxQ
- **API base URL:** `https://api.documint.me/1`

## Authentication

### API Key

Authenticate Documint requests with the API key from your Documint account settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.documint.me/integrations/airtable/airtable-app)

## API conventions

The current page number is read from `current.page`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (5 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:id` | [docs](https://documenter.getpostman.com/view/11741160/TVK5cLxQ) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://documenter.getpostman.com/view/11741160/TVK5cLxQ) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://documenter.getpostman.com/view/11741160/TVK5cLxQ) |
| [Merge Template](actions/merge-template.md) | `POST /templates/:id/content` | [docs](https://documenter.getpostman.com/view/11741160/TVK5cLxQ) |
| [Update Template](actions/update-template.md) | `PUT /templates/:id` | [docs](https://documenter.getpostman.com/view/11741160/TVK5cLxQ) |
