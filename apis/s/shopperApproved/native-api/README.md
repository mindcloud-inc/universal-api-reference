# Shopper Approved: Native API Reference

A consolidated summary of Shopper Approved's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.shopperapproved.com/ui/
- **OpenAPI specification:** https://api.shopperapproved.com/openapi.json
- **API base URL:** `https://api.shopperapproved.com/`

## Authentication

### API Token

Use your Shopper Approved Site ID and API token.

### Credentials

- **API Key:** `apiKey` · required
- **Site ID:** `siteId` · required · The Shopper Approved Site ID for the account.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api)

## Pagination

Use `limit` in the query string to set the page size (default 100; minimum 1). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Review Entry](actions/create-review-entry.md) | `POST /reviews/:siteid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee) |
| [Get Product Aggregate Statistics](actions/get-product-aggregate-statistics.md) | `GET /aggregates/products/:siteid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525) |
| [Get Product Aggregate Statistics by Product ID](actions/get-product-aggregate-statistics-by-product-id.md) | `GET /aggregates/products/:siteid/:productid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525) |
| [Get Review](actions/get-review.md) | `GET /reviews/:siteid/:reviewid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee) |
| [Get Review Aggregate Statistics](actions/get-review-aggregate-statistics.md) | `GET /aggregates/reviews/:siteid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee) |
| [List Product Reviews](actions/list-product-reviews.md) | `GET /products/reviews/:siteid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525) |
| [List Product Reviews by Product or Parent ID](actions/list-product-reviews-by-product-or-parent-id.md) | `GET /products/reviews/:siteid/:productid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_255f306525) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews/:siteid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee) |
| [Update or Cancel Review](actions/update-or-cancel-review.md) | `PUT /reviews/:siteid/:reviewid` | [docs](https://help.shopperapproved.com/en/articles/9796973-how-to-use-our-api#h_d0b7f623ee) |
