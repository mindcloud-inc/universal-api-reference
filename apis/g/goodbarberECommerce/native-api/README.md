# Goodbarber eCommerce: Native API Reference

A consolidated summary of Goodbarber eCommerce's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://commerce.goodbarber.dev/publicapi/v2/documentation/
- **OpenAPI specification:** https://commerce.goodbarber.dev/api/schema_v2/
- **API base URL:** `https://commerce.goodbarber.dev`

## Authentication

### Admin Token

Admin-generated GoodBarber Commerce token plus shop webzine ID.

### Credentials

- **API Token:** `apiKey` · required · GoodBarber Commerce admin token. MindCloud sends this exact value in the required `token` header.
- **Webzine ID:** `webzineId` · required · GoodBarber shop `webzine_id` used in the shared path parameter.

Send these headers with each API request:

```http
token: <apiKey>
```

[Official authentication documentation](https://commerce.goodbarber.dev/publicapi/v2/documentation/)

## Pagination

Use `per_page` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | `POST /publicapi/v2/general/catalog/:webzine_id/product/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Create Variant Option](actions/create-variant-option.md) | `POST /publicapi/v2/general/catalog/:webzine_id/option/` | [docs](https://commerce.goodbarber.dev/api/schema_v2/#tag/Catalog-Option/operation/createOption) |
| [Delete Product](actions/delete-product.md) | `DELETE /publicapi/v2/general/catalog/:webzine_id/product/:product_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Delete Variant Option](actions/delete-variant-option.md) | `DELETE /publicapi/v2/general/catalog/:webzine_id/option/:option_id/` | [docs](https://commerce.goodbarber.dev/api/schema_v2/#tag/Catalog-Option/operation/destroyOption) |
| [Get Collection](actions/get-collection.md) | `GET /publicapi/v2/general/catalog/:webzine_id/collection/:collection_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Customer](actions/get-customer.md) | `GET /publicapi/v2/general/customer/:webzine_id/customer/:customer_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Order](actions/get-order.md) | `GET /publicapi/v2/general/orders/:webzine_id/order/:order_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Order Invoice](actions/get-order-invoice.md) | `GET /publicapi/v2/general/orders/:webzine_id/order/:order_id/invoice/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Order Shipping](actions/get-order-shipping.md) | `GET /publicapi/v2/general/orders/:webzine_id/order/:order_id/shipping/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Page Views Per Week Day](actions/get-page-views-per-week-day.md) | `GET /publicapi/v2/general/stats/:webzine_id/page_views_per_week_day/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Product](actions/get-product.md) | `GET /publicapi/v2/general/catalog/:webzine_id/product/:product_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Product Variant](actions/get-product-variant.md) | `GET /publicapi/v2/general/catalog/:webzine_id/product/:product_id/variant/:variant_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get Prospect](actions/get-prospect.md) | `GET /publicapi/v2/general/customer/:webzine_id/prospect/:user_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Get User Loyalty Points](actions/get-user-loyalty-points.md) | `GET /publicapi/v2/general/marketing/:webzine_id/loyalty/user/:user_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List App Downloads](actions/list-app-downloads.md) | `GET /publicapi/v2/general/stats/:webzine_id/downloads/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List App Global Downloads](actions/list-app-global-downloads.md) | `GET /publicapi/v2/general/stats/:webzine_id/downloads_global/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List App Launches](actions/list-app-launches.md) | `GET /publicapi/v2/general/stats/:webzine_id/launches/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Collections](actions/list-collections.md) | `GET /publicapi/v2/general/catalog/:webzine_id/collection/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Customers](actions/list-customers.md) | `GET /publicapi/v2/general/customer/:webzine_id/customer/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Orders](actions/list-orders.md) | `GET /publicapi/v2/general/orders/:webzine_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Page Views](actions/list-page-views.md) | `GET /publicapi/v2/general/stats/:webzine_id/page_views/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Product Paragraphs](actions/list-product-paragraphs.md) | `GET /publicapi/v2/general/catalog/:webzine_id/product/:product_id/paragraph/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Products](actions/list-products.md) | `GET /publicapi/v2/general/catalog/:webzine_id/product/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Prospects](actions/list-prospects.md) | `GET /publicapi/v2/general/customer/:webzine_id/prospect/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Session Times](actions/list-session-times.md) | `GET /publicapi/v2/general/stats/:webzine_id/session_time/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Tags](actions/list-tags.md) | `GET /publicapi/v2/general/catalog/:webzine_id/tag/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Unique App Launches](actions/list-unique-app-launches.md) | `GET /publicapi/v2/general/stats/:webzine_id/unique_launches/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [List Variant Options](actions/list-variant-options.md) | `GET /publicapi/v2/general/catalog/:webzine_id/option/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Update Product](actions/update-product.md) | `PATCH /publicapi/v2/general/catalog/:webzine_id/product/:product_id/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
| [Update Variant Option](actions/update-variant-option.md) | `PATCH /publicapi/v2/general/catalog/:webzine_id/option/:option_id/` | [docs](https://commerce.goodbarber.dev/api/schema_v2/#tag/Catalog-Option/operation/updateOption) |
| [Validate Front JWT](actions/validate-front-jwt.md) | `POST /publicapi/v2/general/customer/:webzine_id/auth/validate/` | [docs](https://commerce.goodbarber.dev/publicapi/v2/documentation/) |
