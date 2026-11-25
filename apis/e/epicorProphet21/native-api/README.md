# Epicor Prophet 21: Native API Reference

A consolidated summary of Epicor Prophet 21's API configuration and 25 documented operations.

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

Use `$top` in the query string to set the page size (default 25; accepted range 1–5000). Use `$skip` in the query string as the record offset.

## Sorting

Set the sort field with `$orderby` in the query string. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Data View Metadata](actions/get-data-view-metadata.md) | `GET /data/erp/views/v1/$metadata` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [Get Data View Record](actions/get-data-view-record.md) | `GET /data/erp/views/v1/:view(:key)` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [Get Manifest Metadata](actions/get-manifest-metadata.md) | `GET /data/manifest/v1/$metadata` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [Get OData Table Metadata](actions/get-odata-table-metadata.md) | `GET /odataservice/odata/table/$metadata` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [Get OData View Metadata](actions/get-odata-view-metadata.md) | `GET /odataservice/odata/view/$metadata` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#endpoints) |
| [List Addresses](actions/list-addresses.md) | `GET /data/erp/views/v1/p21_view_address` |  |
| [List Contacts](actions/list-contacts.md) | `GET /data/erp/views/v1/p21_view_contacts` |  |
| [List Customers](actions/list-customers.md) | `GET /data/erp/views/v1/p21_view_customer` |  |
| [List Data Views](actions/list-data-views.md) | `GET /data/erp/views/v1` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [List Entity Addresses](actions/list-entity-addresses.md) | `GET /api/entity/addresses` |  |
| [List Entity Contacts](actions/list-entity-contacts.md) | `GET /api/entity/contacts` |  |
| [List Entity Customers](actions/list-entity-customers.md) | `GET /api/entity/customers/` |  |
| [List Manifest Collections](actions/list-manifest-collections.md) | `GET /data/manifest/v1/` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [List OData Tables](actions/list-odata-tables.md) | `GET /odataservice/odata/table/` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [List OData Views](actions/list-odata-views.md) | `GET /odataservice/odata/view/` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [List Order Lines](actions/list-order-lines.md) | `GET /data/erp/views/v1/p21_view_oe_line` |  |
| [List Product Groups](actions/list-product-groups.md) | `GET /data/erp/views/v1/p21_view_product_group` |  |
| [List Quotes](actions/list-quotes.md) | `GET /data/erp/views/v1/p21_view_oe_hdr` |  |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /data/erp/views/v1/p21_view_oe_hdr` |  |
| [Query Data View](actions/query-data-view.md) | `GET /data/erp/views/v1/:view` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#the-other-odata-surface-data-erp-views-v1) |
| [Query Manifest Collection](actions/query-manifest-collection.md) | `GET /data/manifest/v1/:collection` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
| [Query OData Table](actions/query-odata-table.md) | `GET /odataservice/odata/table/:tableName` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#endpoints) |
| [Query OData Table with Body](actions/query-odata-table-with-body.md) | `POST /odataservice/odata/table/:tableName/$query` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#long-filters-and-post-query) |
| [Query OData View](actions/query-odata-view.md) | `GET /odataservice/odata/view/:viewName` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html#endpoints) |
| [Query OData View with Body](actions/query-odata-view-with-body.md) | `POST /odataservice/odata/view/:viewName/$query` | [docs](https://mrwuss.github.io/p21-api-documentation/html/02-OData-API.html) |
