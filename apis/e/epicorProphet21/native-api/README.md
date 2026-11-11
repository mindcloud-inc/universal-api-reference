# Epicor Prophet 21: Native API Reference

A consolidated summary of Epicor Prophet 21's API configuration and 11 documented operations.

- **API base URL:** `{apiUrl}`

## Authentication

### Prophet 21 username and password

Sign in to your Prophet 21 API using the same API URL, username, and password as the existing Epicor integration.

### Credentials

- **API URL:** `apiUrl` · required · The API base URL used by your existing Epicor integration.
- **Username:** `username` · required
- **Password:** `password` · required

Send these headers with each API request:

```http
Authorization: Bearer <custom.accessToken>
password: <password>
username: <username>
```

## Pagination

Use `$top` in the query string to set the page size (default 25; accepted range 25–5000). Use `$skip` in the query string as the record offset.

## Endpoints (11 documented)

| Operation | Method & path |
| --- | --- |
| [List Addresses](actions/list-addresses.md) | `GET /data/erp/views/v1/p21_view_address` |
| [List Contacts](actions/list-contacts.md) | `GET /data/erp/views/v1/p21_view_contacts` |
| [List Customers](actions/list-customers.md) | `GET /data/erp/views/v1/p21_view_customer` |
| [List Entity Addresses](actions/list-entity-addresses.md) | `GET /api/entity/addresses` |
| [List Entity Contacts](actions/list-entity-contacts.md) | `GET /api/entity/contacts` |
| [List Entity Customers](actions/list-entity-customers.md) | `GET /api/entity/customers/` |
| [List Order Lines](actions/list-order-lines.md) | `GET /data/erp/views/v1/p21_view_oe_line` |
| [List Product Groups](actions/list-product-groups.md) | `GET /data/erp/views/v1/p21_view_product_group` |
| [List Quotes](actions/list-quotes.md) | `GET /data/erp/views/v1/p21_view_oe_hdr` |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /data/erp/views/v1/p21_view_oe_hdr` |
| [Query Data View](actions/query-data-view.md) | `GET /data/erp/views/v1/:view` |
