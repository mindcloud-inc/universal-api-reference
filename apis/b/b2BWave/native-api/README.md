# B2B Wave: Native API Reference

A consolidated summary of B2B Wave's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs.b2bwave.com/category/97-api
- **API base URL:** `{storeUrl}/api`

## Authentication

### API Key

Connect using a B2B Wave API key and store URL.

### Credentials

- **API Key:** `apiKey` · required
- **Store URL:** `storeUrl` · required · Root URL of your B2B Wave store, for example https://yourstore.b2bwave.com.

Send these headers with each API request:

```http
Authorization: Token token="<apiKey>"
```

[Official authentication documentation](https://docs.b2bwave.com/article/111-b2b-wave-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | `GET /addressbooks` | [docs](https://docs.b2bwave.com/article/102-address-books) |
| [List Brands](actions/list-brands.md) | `GET /brands` | [docs](https://docs.b2bwave.com/article/139-brands) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://docs.b2bwave.com/article/103-categories) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.b2bwave.com/article/101-customers) |
| [List Options](actions/list-options.md) | `GET /options` | [docs](https://docs.b2bwave.com/article/246-options-api) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /status_orders/` | [docs](https://docs.b2bwave.com/article/164-order-statuses) |
| [List Price Lists](actions/list-price-lists.md) | `GET /pricelists` | [docs](https://docs.b2bwave.com/article/100-pricelists) |
| [List Product Customer Prices](actions/list-product-customer-prices.md) | `GET /product_customer_prices` | [docs](https://docs.b2bwave.com/article/107-product-customer-prices) |
| [List Product Discounts](actions/list-product-discounts.md) | `GET /product_discounts` | [docs](https://docs.b2bwave.com/article/205-product-discounts-api) |
| [List Product Prices](actions/list-product-prices.md) | `GET /product_prices` | [docs](https://docs.b2bwave.com/article/106-product-prices) |
| [List Product Statuses](actions/list-product-statuses.md) | `GET /status_products` | [docs](https://docs.b2bwave.com/article/104-products-status) |
| [List Product Variants](actions/list-product-variants.md) | `GET /product_variants` | [docs](https://docs.b2bwave.com/article/245-product-variants-api) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.b2bwave.com/article/105-products) |
| [List Sales Reps](actions/list-sales-reps.md) | `GET /sales_reps` | [docs](https://docs.b2bwave.com/article/108-sales-reps) |
| [List Shipping Options](actions/list-shipping-options.md) | `GET /shipping_options` | [docs](https://docs.b2bwave.com/article/169-shipping-options) |
| [List Suppliers](actions/list-suppliers.md) | `GET /suppliers` | [docs](https://docs.b2bwave.com/article/250-suppliers-api) |
| [List VAT Classes](actions/list-vat-classes.md) | `GET /vat_classes` | [docs](https://docs.b2bwave.com/article/99-vat-classes) |
| [List VAT Groups](actions/list-vat-groups.md) | `GET /vat_groups` | [docs](https://docs.b2bwave.com/article/98-vat-groups) |
| [List VAT Rates](actions/list-vat-rates.md) | `GET /vat_rates` | [docs](https://docs.b2bwave.com/article/154-vat-rates) |
| [List VAT Rules](actions/list-vat-rules.md) | `GET /vat_rules` | [docs](https://docs.b2bwave.com/article/155-vat-rules) |
