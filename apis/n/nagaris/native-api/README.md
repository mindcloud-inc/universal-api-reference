# Nagaris: Native API Reference

A consolidated summary of Nagaris's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://core.nagaris.com/api/v1/schema/redoc/
- **OpenAPI specification:** https://core.nagaris.com/api/v1/schema/
- **API base URL:** `https://core.nagaris.com/api/v1`

## Authentication

### Bearer Token

Paste the raw Nagaris bearer access token only, without the Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://core.nagaris.com/api/v1/schema/redoc/)

## Pagination

Use `page_size` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Client Groups](actions/list-client-groups.md) | `GET /client-groups/` | [docs](https://core.nagaris.com/api/v1/schema/redoc/#tag/client-groups/operation/list_client_groups) |
