# OneHash ERP: Native API Reference

A consolidated summary of OneHash ERP's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.frappe.io/framework/user/en/api/rest
- **API base URL:** `https://{siteName}.onehash.ai`

## Authentication

### API token

Use a OneHash ERP API token in the format api_key:api_secret. The runtime sends it as Authorization: token <api_key:api_secret>.

### Credentials

- **API Key:** `apiKey` · required
- **Site Name:** `siteName` · required · Tenant site subdomain before .onehash.ai, for example mindcloud.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.frappe.io/framework/user/en/api/rest)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit_page_length` in the query string to set the page size (default 20; accepted range 1–100). Use `limit_start` in the query string as the record offset; numbering starts at 0.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | `GET /api/resource/Customer` | [docs](https://docs.frappe.io/framework/user/en/api/rest) |
