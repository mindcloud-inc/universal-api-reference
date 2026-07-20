# WiserReview: Native API Reference

A consolidated summary of WiserReview's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.wiserreview.com
- **API base URL:** `https://api.wiserreview.com/api/v1`

## Authentication

### API Token

Use a WiserReview auth token generated from your dashboard API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://apidocs.wiserreview.com/generate-token-26189664e0)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Review](actions/create-review.md) | `POST /createReview` | [docs](https://apidocs.wiserreview.com/create-review-26260657e0) |
| [Generate Token](actions/generate-token.md) | `GET /authToken` | [docs](https://apidocs.wiserreview.com/generate-token-26189664e0) |
| [Get Product Review Data](actions/get-product-review-data.md) | `POST https://rs.wiserreview.com/api/v1/getProductReviewData` | [docs](https://apidocs.wiserreview.com/product-review-26682568e0) |
| [Get Star Ratings](actions/get-star-ratings.md) | `POST https://rs.wiserreview.com/api/v1/getStarRating` | [docs](https://apidocs.wiserreview.com/star-rating-26671212e0) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://apidocs.wiserreview.com/get-review-list-26190892e0) |
| [List Reviews By Product](actions/list-reviews-by-product.md) | `GET /reviewsByProduct` | [docs](https://apidocs.wiserreview.com/get-reviews-by-product-26190894e0) |
