# Veedea: Native API Reference

A consolidated summary of Veedea's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://veedea.com/api/doc
- **API base URL:** `https://veedea.com/api`

## Authentication

### API Key

Use the Veedea API key from the Profile page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://veedea.com/api/doc)

## API conventions

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Auth Token](actions/get-auth-token.md) | `GET /auth` | [docs](https://veedea.com/api/doc) |
| [List Campaigns](actions/list-campaigns.md) | `GET /getcampaign` | [docs](https://veedea.com/api/doc) |
| [List Leads](actions/list-leads.md) | `GET /getleads` | [docs](https://veedea.com/api/doc) |
