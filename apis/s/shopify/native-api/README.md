# Shopify: Native API Reference

A consolidated summary of Shopify's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://shopify.dev/docs/api
- **REST base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **GraphQL base URL:** `https://{storeName}.myshopify.com/admin/api/`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Store Name:** `storeName` · optional

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

### OAuth 2.0

### Credentials

- **Store Name:** `storeName` · required
- **Client ID:** `clientID` · required
- **Client Secret:** `clientSecret` · required

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://{{credentials.storeName}}.myshopify.com/admin/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.storeName}}.myshopify.com/admin/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read_customers,write_customers,write_draft_orders,read_draft_orders,write_inventory,read_inventory,read_orders,write_orders,read_product_feeds,write_product_feeds,read_product_listings,write_product_listings,read_products,write_products,customer_read_companies,customer_write_companies,customer_write_customers,customer_read_customers,customer_read_orders,customer_write_orders,read_all_orders,read_returns`.

Refresh expired access tokens with a POST request to https://{{credentials.storeName}}.myshopify.com/admin/oauth/access_token.

[Official authentication documentation](https://shopify.dev/docs/api/usage/authentication)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

### GraphQL

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

- **REST:** Use `limit` in the request body to set the page size (default 20; accepted range 1–250). Use `cursor` in the request body as the pagination cursor.
- **GraphQL:** Use `limit` in the request parameters to set the page size (default 50; accepted range 1–250). Use `cursor` in the request parameters as the pagination cursor.

## Sorting

- **GraphQL:** Send sorting in the request body. Only one sort field is accepted.

## Retry behavior

- **REST:** Multiply the delay by 2 after each failed attempt.

## Endpoints (17 documented)

| Operation | API | Method & path | Vendor docs |
| --- | --- | --- | --- |
| [Activate Inventory Item](actions/activate-inventory-item.md) | GraphQL | `POST /:apiVersion/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/mutations/inventoryActivate) |
| [Create Webhook Subscription (HTTP)](actions/create-webhook-subscription-http.md) | REST | `POST 2024-10/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/mutations/webhookSubscriptionCreate) |
| [Get Product Variant by SKU](actions/get-product-variant-by-sku.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/productVariants) |
| [GraphQL - Get Records (Paginated)](actions/graphql-get-records-paginated.md) | REST | `POST :version/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest) |
| [GraphQL - Get Records (Unwrapped Edges)](actions/graphql-get-records-unwrapped-edges.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest) |
| [List All Orders](actions/list-all-orders-graphql.md) | REST | `POST 2025-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/orders) |
| [List Companies](actions/list-companies-graphql.md) | REST | `POST 2025-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/companies) |
| [List Customers](actions/list-customers-graphql.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/customers) |
| [List Deleted Product Events](actions/list-deleted-product-events.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/unstable/queries/events) |
| [List Locations](actions/list-locations.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/locations) |
| [List Orders](actions/list-orders.md) | REST | `POST 2025-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/orders) |
| [List Product Variants](actions/list-product-variants.md) | GraphQL | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/productVariants) |
| [List Products](actions/list-products.md) | GraphQL | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/products) |
| [List Publication Channels](actions/list-publication-channels.md) | REST | `POST 2026-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/publications) |
| [List Selling Plan Groups](actions/list-selling-plan-groups.md) | REST | `POST 2024-10/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/queries/sellingPlanGroups) |
| [Get Order Transactions (GraphQL)](actions/update-product-graph-ql.md) | REST | `POST 2025-01/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest) |
| [Update Product (GraphQL)](actions/update-product-graphql.md) | REST | `POST 2024-07/graphql.json` | [docs](https://shopify.dev/docs/api/admin-graphql/latest/mutations/productSet) |
