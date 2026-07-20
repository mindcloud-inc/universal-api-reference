# AdvantShop: Native API Reference

A consolidated summary of AdvantShop's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.advantshop.net/api
- **API base URL:** `{baseUrl}`

## Authentication

### API Key

Use an AdvantShop store API key. AdvantShop documents API requests with the shared query parameter `apikey`.

### Credentials

- **API Key:** `apiKey` · required
- **Store API Base URL:** `baseUrl` · required · The AdvantShop store API root URL ending in /api, for example https://your-store.example/api.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.advantshop.net/help/pages/how-to-use-api)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Search](actions/autocomplete-search.md) | `POST /search/autocomplete` | [docs](https://www.advantshop.net/api) |
| [Calculate Product Price](actions/calculate-product-price.md) | `POST /products/{id}/price` | [docs](https://www.advantshop.net/api) |
| [Change Order Status](actions/change-order-status.md) | `POST /order/changestatus` | [docs](https://www.advantshop.net/api) |
| [Count Catalog Filter Products](actions/count-catalog-filter-products.md) | `POST /catalog/filtercount` | [docs](https://www.advantshop.net/api) |
| [Count Search Filter Products](actions/count-search-filter-products.md) | `POST /search/filtercount` | [docs](https://www.advantshop.net/api) |
| [Create Category](actions/create-category.md) | `POST /categories/add` | [docs](https://www.advantshop.net/api) |
| [Create Customer](actions/create-customer.md) | `POST /customers/add` | [docs](https://www.advantshop.net/api) |
| [Create Lead](actions/create-lead.md) | `POST /leads/add` | [docs](https://www.advantshop.net/api) |
| [Get Bonus Card](actions/get-bonus-card.md) | `GET /bonus-cards/{id}` | [docs](https://www.advantshop.net/api) |
| [Get Bonus Card Settings](actions/get-bonus-card-settings.md) | `GET /bonus-cards/settings` | [docs](https://www.advantshop.net/api) |
| [Get Catalog](actions/get-catalog.md) | `POST /catalog` | [docs](https://www.advantshop.net/api) |
| [Get Catalog Filter](actions/get-catalog-filter.md) | `POST /catalog/filter` | [docs](https://www.advantshop.net/api) |
| [Get Category](actions/get-category.md) | `GET /categories/{id}` | [docs](https://www.advantshop.net/api) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{id}` | [docs](https://www.advantshop.net/api) |
| [Get Customer Bonuses](actions/get-customer-bonuses.md) | `GET /customers/{id}/bonuses` | [docs](https://www.advantshop.net/api) |
| [Get Full Catalog](actions/get-full-catalog.md) | `POST /catalog/all` | [docs](https://www.advantshop.net/api) |
| [Get Order](actions/get-order.md) | `GET /order/get/{id}` | [docs](https://www.advantshop.net/api) |
| [Get Product](actions/get-product.md) | `GET /products/{id}` | [docs](https://www.advantshop.net/api) |
| [Get Product Properties](actions/get-product-properties.md) | `GET /products/{id}/properties` | [docs](https://www.advantshop.net/api) |
| [Get Search Filter](actions/get-search-filter.md) | `POST /search/filter` | [docs](https://www.advantshop.net/api) |
| [Get Settings](actions/get-settings.md) | `GET /settings` | [docs](https://www.advantshop.net/api) |
| [Initialize Store](actions/initialize-store.md) | `GET /init` | [docs](https://www.advantshop.net/api) |
| [List Bonus Card Transactions](actions/list-bonus-card-transactions.md) | `GET /bonus-cards/{id}/transactions` | [docs](https://www.advantshop.net/api) |
| [List Bonus Grades](actions/list-bonus-grades.md) | `GET /bonus-grades` | [docs](https://www.advantshop.net/api) |
| [List Carousels](actions/list-carousels.md) | `GET /carousels` | [docs](https://www.advantshop.net/api) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://www.advantshop.net/api) |
| [List Customer Groups](actions/list-customer-groups.md) | `GET /customergroups` | [docs](https://www.advantshop.net/api) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.advantshop.net/api) |
| [List Leads](actions/list-leads.md) | `POST /leads/getlist` | [docs](https://www.advantshop.net/api) |
| [List Managers](actions/list-managers.md) | `GET /managers` | [docs](https://www.advantshop.net/api) |
| [List Order Statuses](actions/list-order-statuses.md) | `POST /orderstatus/getlist` | [docs](https://www.advantshop.net/api) |
| [List Orders](actions/list-orders.md) | `POST /order/getlist` | [docs](https://www.advantshop.net/api) |
| [List Product Gifts](actions/list-product-gifts.md) | `GET /products/{id}/gifts` | [docs](https://www.advantshop.net/api) |
| [List Product Reviews](actions/list-product-reviews.md) | `GET /products/{id}/reviews` | [docs](https://www.advantshop.net/api) |
| [List Product Stocks](actions/list-product-stocks.md) | `GET /products/{id}/stocks` | [docs](https://www.advantshop.net/api) |
| [List Related Products](actions/list-related-products.md) | `GET /products/{id}/related-products` | [docs](https://www.advantshop.net/api) |
| [Search Catalog](actions/search-catalog.md) | `POST /search` | [docs](https://www.advantshop.net/api) |
| [Set Order Paid](actions/set-order-paid.md) | `POST /order/setpaid` | [docs](https://www.advantshop.net/api) |
| [Update Category](actions/update-category.md) | `POST /categories/{id}` | [docs](https://www.advantshop.net/api) |
| [Update Customer](actions/update-customer.md) | `POST /customers/{id}` | [docs](https://www.advantshop.net/api) |
