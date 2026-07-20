# Yeahdesk: Native API Reference

A consolidated summary of Yeahdesk's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://help.yeahdesk.ru/docs/for-developers/http-api
- **API base URL:** `https://app.yeahdesk.ru/api`

## Authentication

### API key

Use a Yeahdesk API token in the token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.yeahdesk.ru/docs/for-developers/http-api/api-auth)

## Pagination

Use `limit` in the query string to set the page size (default 50). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List contacts](actions/list-contacts.md) | `GET /clients/person/read` | [docs](https://help.yeahdesk.ru/docs/for-developers/http-api/contacts) |
