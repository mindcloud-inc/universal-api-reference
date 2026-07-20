# Dukaan: Native API Reference

A consolidated summary of Dukaan's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/25389466/2s9Yynk3f7
- **API base URL:** `https://api.mydukaan.io`

## Authentication

### API Key

Use a Dukaan store authentication token generated from web.mydukaan.io developer settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 30; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `ordering` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Customer Tag](actions/add-customer-tag.md) | `POST api/store/seller/:storeUuid/tags/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Customer](actions/create-customer.md) | `POST api/campaign/seller/store-lead/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Customer Tag Definition](actions/create-customer-tag-definition.md) | `POST api/store/seller/:storeUuid/store-tags/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Discount](actions/create-discount.md) | `POST api/coupon/seller/coupon/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Order](actions/create-order.md) | `POST api/order/seller/order/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Product](actions/create-product.md) | `POST api/product/seller/:storeUuid/product/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Product Category](actions/create-product-category.md) | `POST api/product/seller/product-category/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Product With Variants](actions/create-product-with-variants.md) | `POST api/product/seller/:storeUuid/product/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Create Warehouse](actions/create-warehouse.md) | `POST api/store/seller/store-warehouse/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Get Customer Details](actions/get-customer-details.md) | `GET api/campaign/seller/store-lead/v2/store-lead-data/:storeLeadId/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Get Order](actions/get-order.md) | `GET api/order/seller/:orderUuid/order/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Get Product](actions/get-product.md) | `GET api/product/seller/:storeUuid/product/:productUuid/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Discounts](actions/list-discounts.md) | `GET api/coupon/seller/coupon/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Inventory Products](actions/list-inventory-products.md) | `GET api/product/seller/:storeUuid/product/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Orders](actions/list-orders.md) | `GET api/seller-front/order-list/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Product Categories](actions/list-product-categories.md) | `GET api/product/seller/product-category/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Products](actions/list-products.md) | `GET api/seller-front/:storeUuid/product-list/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Products By Category](actions/list-products-by-category.md) | `GET api/seller-front/:storeUuid/product-list/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Store Audience](actions/list-store-audience.md) | `GET api/store/seller/store-buyer/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [List Warehouses](actions/list-warehouses.md) | `GET api/store/seller/store-warehouse/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Search Orders](actions/search-orders.md) | `GET api/seller-front/order-list/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Search Product Categories](actions/search-product-categories.md) | `GET api/product/seller/product-category/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Search Products](actions/search-products.md) | `GET api/seller-front/:storeUuid/product-list/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Customer Notes](actions/update-customer-notes.md) | `PATCH api/order/seller/:storeLeadId/update-storelead-notes/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Inventory](actions/update-inventory.md) | `PATCH api/store/seller/seller-warehouse-inventory/:inventoryItemUuid/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Order Status](actions/update-order-status.md) | `PATCH api/order/seller/:orderUuid/order/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Product](actions/update-product.md) | `PATCH api/product/seller/:storeUuid/product/:productUuid/v2/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Product Category](actions/update-product-category.md) | `PATCH api/product/seller/:categoryUuid/product-category/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
| [Update Warehouse](actions/update-warehouse.md) | `PATCH api/store/seller/store-warehouse/v2/:warehouseUuid/` | [docs](https://documenter.getpostman.com/view/25389466/2s9Yynk3f7) |
