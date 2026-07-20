# G2: Native API Reference

A consolidated summary of G2's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://data.g2.com/api/docs
- **OpenAPI specification:** https://data.g2.com/openapi/v2.yaml
- **API base URL:** `https://data.g2.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documentation.g2.com/docs/developer-portal#access-tokens)

### OAuth 2.0

Connect G2 using OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.g2.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.g2.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.g2.com/oauth/token.

[Official authentication documentation](https://documentation.g2.com/docs/developer-portal)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`. The total page count is read from `meta.recordCount`.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; maximum 100). Use `page[after]` in the query string as the pagination cursor.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Browse Product Buyer Intent](actions/browse-product-buyer-intent.md) | `GET /api/v2/products/:subject_product_id/buyer_intent` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [Get Category](actions/get-category.md) | `GET /api/v2/categories/:id` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [Get Product](actions/get-product.md) | `GET /api/v2/products/:product_id` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [Get Question](actions/get-question.md) | `GET /api/v2/questions/:id` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [Get Vendor](actions/get-vendor.md) | `GET /api/v2/vendors/:id` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [List Categories](actions/list-categories.md) | `GET /api/v2/categories` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [List Products](actions/list-products.md) | `GET /api/v2/products` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [List Questions](actions/list-questions.md) | `GET /api/v2/questions` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [List Vendors](actions/list-vendors.md) | `GET /api/v2/vendors` | [docs](https://data.g2.com/openapi/v2.yaml) |
| [Retrieve Market Signals](actions/retrieve-market-signals.md) | `GET /api/v2/market_signals` | [docs](https://data.g2.com/openapi/v2.yaml) |
