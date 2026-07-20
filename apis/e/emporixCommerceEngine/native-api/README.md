# Emporix Commerce Engine: Native API Reference

A consolidated summary of Emporix Commerce Engine's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.emporix.io/api-references/api-guides/api-guides-and-references
- **API base URL:** `https://api.emporix.io`

## Authentication

### OAuth 2.0 Client Credentials

Use Emporix OAuth2 client credentials to request service access tokens for a tenant.

### Credentials

- **Tenant ID:** `tenantId` · required · Emporix tenant name used in OAuth token scope and tenant-scoped resource paths. Use the lowercase tenant ID from the Emporix Developer Portal.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://api.emporix.io/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `customermanagement.legalentity_read customermanagement.legalentity_read_own order.order_manage_by_vendor order.order_read order.order_read_by_vendor order.order_update order.order_update_completed price.price_manage price.price_read price.pricelist_read product.product_manage product.product_template_read`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/authentication/oauth-service/api-reference/api.yml)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–100). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Cart Item](actions/add-cart-item.md) | `POST /cart/{{credentials.tenantId}}/carts/:cartId/items` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [Create Cart](actions/create-cart.md) | `POST /cart/{{credentials.tenantId}}/carts` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [Create Catalog](actions/create-catalog.md) | `POST /catalog/{{credentials.tenantId}}/catalogs` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/catalog/api-reference/api.yml) |
| [Create Product](actions/create-product.md) | `POST /product/{{credentials.tenantId}}/products` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [Get Brand](actions/get-brand.md) | `GET /brand/brands/:brandId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/brand-service/api-reference/api.yml) |
| [Get Cart](actions/get-cart.md) | `GET /cart/{{credentials.tenantId}}/carts/:cartId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [Get Catalog](actions/get-catalog.md) | `GET /catalog/{{credentials.tenantId}}/catalogs/:catalogId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/catalog/api-reference/api.yml) |
| [Get Category](actions/get-category.md) | `GET /category/{{credentials.tenantId}}/categories/:categoryId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/category-tree/api-reference/api.yml) |
| [Get Label](actions/get-label.md) | `GET /labels/:labelId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/label-service/api-reference/api.yml) |
| [Get Legal Entity](actions/get-legal-entity.md) | `GET /customer-management/{{credentials.tenantId}}/legal-entities/:legalEntityId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/companies-and-customers/client-management/api-reference/api.yml) |
| [Get Price](actions/get-price.md) | `GET /price/{{credentials.tenantId}}/prices/:priceId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [Get Price List](actions/get-price-list.md) | `GET /price/{{credentials.tenantId}}/price-lists/:priceListId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [Get Product](actions/get-product.md) | `GET /product/{{credentials.tenantId}}/products/:productId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [Get Sales Order](actions/get-sales-order.md) | `GET /order-v2/{{credentials.tenantId}}/salesorders/:orderId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml) |
| [List Brands](actions/list-brands.md) | `GET /brand/brands` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/brand-service/api-reference/api.yml) |
| [List Cart Items](actions/list-cart-items.md) | `GET /cart/{{credentials.tenantId}}/carts/:cartId/items` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [List Carts](actions/list-carts.md) | `GET /cart/{{credentials.tenantId}}/carts` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [List Catalogs](actions/list-catalogs.md) | `GET /catalog/{{credentials.tenantId}}/catalogs` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/catalog/api-reference/api.yml) |
| [List Categories](actions/list-categories.md) | `GET /category/{{credentials.tenantId}}/categories` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/category-tree/api-reference/api.yml) |
| [List Category Trees](actions/list-category-trees.md) | `GET /category/{{credentials.tenantId}}/category-trees` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/category-tree/api-reference/api.yml) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/label-service/api-reference/api.yml) |
| [List Legal Entities](actions/list-legal-entities.md) | `GET /customer-management/{{credentials.tenantId}}/legal-entities` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/companies-and-customers/client-management/api-reference/api.yml) |
| [List Order Transitions](actions/list-order-transitions.md) | `GET /order-v2/{{credentials.tenantId}}/salesorders/:orderId/transitions` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml) |
| [List Price Lists](actions/list-price-lists.md) | `GET /price/{{credentials.tenantId}}/price-lists` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [List Prices](actions/list-prices.md) | `GET /price/{{credentials.tenantId}}/prices` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [List Product Templates](actions/list-product-templates.md) | `GET /product/{{credentials.tenantId}}/product-templates` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [List Products](actions/list-products.md) | `GET /product/{{credentials.tenantId}}/products` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [List Sales Orders](actions/list-sales-orders.md) | `GET /order-v2/{{credentials.tenantId}}/salesorders` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml) |
| [List Site Availability](actions/list-site-availability.md) | `GET /availability/{{credentials.tenantId}}/availability/site/:site` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/availability/api-reference/api.yml) |
| [Match Prices](actions/match-prices.md) | `POST /price/{{credentials.tenantId}}/match-prices` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [Patch Product](actions/patch-product.md) | `PATCH /product/{{credentials.tenantId}}/products/:productId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [Search Carts](actions/search-carts.md) | `POST /cart/{{credentials.tenantId}}/carts/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
| [Search Categories](actions/search-categories.md) | `POST /category/{{credentials.tenantId}}/categories/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/catalogs-and-categories/category-tree/api-reference/api.yml) |
| [Search Legal Entities](actions/search-legal-entities.md) | `POST /customer-management/{{credentials.tenantId}}/legal-entities/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/companies-and-customers/client-management/api-reference/api.yml) |
| [Search Prices](actions/search-prices.md) | `POST /price/{{credentials.tenantId}}/prices/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml) |
| [Search Products](actions/search-products.md) | `POST /product/{{credentials.tenantId}}/products/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [Search Sales Orders](actions/search-sales-orders.md) | `POST /order-v2/{{credentials.tenantId}}/salesorders/search` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml) |
| [Update Order Status](actions/update-order-status.md) | `POST /order-v2/{{credentials.tenantId}}/salesorders/:orderId/transitions` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/orders/order/api-reference/api.yml) |
| [Upsert Product](actions/upsert-product.md) | `PUT /product/{{credentials.tenantId}}/products/:productId` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/products-labels-and-brands/product-service/api-reference/api.yml) |
| [Validate Cart](actions/validate-cart.md) | `GET /cart/{{credentials.tenantId}}/carts/:cartId/validate` | [docs](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/checkout/cart/api-reference/api.yml) |
