# Catalog Machine: Native API Reference

A consolidated summary of Catalog Machine's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://help.catalogmachine.com/en/collections/1889860-automation-api
- **API base URL:** `https://www.catalogmachine.com/api/v1`

## Authentication

### API Key

Catalog Machine REST API authentication via API key from Automation > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `products`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–250). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:code` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Delete Products (Bulk)](actions/delete-products-bulk.md) | `DELETE /products` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Get Import Job Status](actions/get-import-job-status.md) | `GET /jobs/import/:jobId` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Get Product](actions/get-product.md) | `GET /products/:code` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Import CSV Content](actions/import-csv-content.md) | `POST /import/csv` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [List Catalogs](actions/list-catalogs.md) | `GET /catalogs` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Rebuild Catalog PDF](actions/rebuild-catalog-pdf.md) | `GET /catalogs/:permalink/rebuild` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Start Shopify Import](actions/start-shopify-import.md) | `GET /import/shopify/sync` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Upsert Product](actions/upsert-product.md) | `POST /products/:code` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
| [Upsert Products (Bulk)](actions/upsert-products-bulk.md) | `POST /products` | [docs](https://help.catalogmachine.com/en/articles/3667421-rest-api) |
