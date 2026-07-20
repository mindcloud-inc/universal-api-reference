# Omnisend: Native API Reference

A consolidated summary of Omnisend's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.omnisend.com/reference/getting-started
- **API base URL:** `https://api.omnisend.com`

## Authentication

### API Key

Use your Omnisend API key. Omnisend expects it in the X-API-KEY header, not as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required · Paste the Omnisend API key from your Omnisend account.

[Official authentication documentation](https://support.omnisend.com/en/articles/1061890-generate-an-api-key-in-omnisend)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `paging.next`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Batch](actions/create-batch.md) | `POST /v5/batches` | [docs](https://api-docs.omnisend.com/reference/post_batches) |
| [Create Category](actions/create-category.md) | `POST /v5/product-categories` | [docs](https://api-docs.omnisend.com/reference/post_product-categories) |
| [Create Contact](actions/create-contact.md) | `POST /v5/contacts` | [docs](https://api-docs.omnisend.com/reference/post_contacts) |
| [Create Product](actions/create-product.md) | `POST /v5/products` | [docs](https://api-docs.omnisend.com/reference/post_products) |
| [Delete Product](actions/delete-product.md) | `DELETE /v5/products/:productID` | [docs](https://api-docs.omnisend.com/reference/delete_products-productid) |
| [Get Cart](actions/get-cart.md) | `GET /v3/carts/:cartID` | [docs](https://api-docs.omnisend.com/v3/reference/get_carts-cartid) |
| [Get Contact](actions/get-contact.md) | `GET /v5/contacts/:contactID` | [docs](https://api-docs.omnisend.com/reference/get_contacts-contactid) |
| [Get Order](actions/get-order.md) | `GET /v3/orders/:orderID` | [docs](https://api-docs.omnisend.com/v3/reference/get_orders-orderid) |
| [Get Product](actions/get-product.md) | `GET /v5/products/:productID` | [docs](https://api-docs.omnisend.com/reference/get_products-productid) |
| [List Carts](actions/list-carts.md) | `GET /v3/carts` | [docs](https://api-docs.omnisend.com/v3/reference/get_carts) |
| [List Categories](actions/list-categories.md) | `GET /v5/product-categories` | [docs](https://api-docs.omnisend.com/reference/get_product-categories) |
| [List Contacts](actions/list-contacts.md) | `GET /v5/contacts` | [docs](https://api-docs.omnisend.com/reference/get_contacts) |
| [List Custom Events](actions/list-custom-events.md) | `GET /v3/events` | [docs](https://api-docs.omnisend.com/v3/reference/get_events) |
| [List Orders](actions/list-orders.md) | `GET /v3/orders` | [docs](https://api-docs.omnisend.com/v3/reference/get_orders) |
| [List Products](actions/list-products.md) | `GET /v5/products` | [docs](https://api-docs.omnisend.com/reference/get_products) |
| [Replace Product](actions/replace-product.md) | `PUT /v5/products/:productID` | [docs](https://api-docs.omnisend.com/reference/put_products-productid) |
| [Trigger Custom Event](actions/trigger-custom-event.md) | `POST /v5/events` | [docs](https://api-docs.omnisend.com/reference/post_events) |
| [Update Category](actions/update-category.md) | `PATCH /v5/product-categories/:categoryID` | [docs](https://api-docs.omnisend.com/reference/patch_product-categories-categoryid) |
| [Update Contact](actions/update-contact.md) | `PATCH /v5/contacts/:contactID` | [docs](https://api-docs.omnisend.com/reference/patch_contacts-contactid) |
