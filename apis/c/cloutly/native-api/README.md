# Cloutly: Native API Reference

A consolidated summary of Cloutly's API configuration and 7 documented operations, with links to official documentation.

- **Official docs:** https://docs.cloutly.com/reviews-sdk-for-marketplace-websites
- **REST API base URL:** `https://app.cloutly.com/api/v1`
- **REST API base URL:** `https://marketplace.cloutly.com/api/v2`

## Authentication

### API Key

Authenticate Cloutly REST API requests with an API key from Settings -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/introduction/authentication)

## API conventions

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

- **REST API:** Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Sorting

- **REST API:** Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (7 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Business](actions/create-business.md) | `POST https://marketplace.cloutly.com/api/v2/businesses` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-create-business) |
| [Get Business](actions/get-business.md) | `GET https://marketplace.cloutly.com/api/v2/businesses/:businessId` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-get-business) |
| [Get Business OAuth Link](actions/get-business-oauth-link.md) | `POST https://marketplace.cloutly.com/api/v2/businesses/:businessId/auth-link` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/business-api/business-api-get-business-oauth-link) |
| [Health Check](actions/health-check.md) | `GET /ping` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/introduction/ping) |
| [List Businesses](actions/list-businesses.md) | `GET /businesses` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/rest-api/review-summary) |
| [List Reviews](actions/list-reviews.md) | `GET /reviews` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/rest-api/list-reviews) |
| [Send Review Invite](actions/send-review-invite.md) | `POST /send-review-invite` | [docs](https://docs.cloutly.com/reviews-sdk-for-marketplace-websites/rest-api/invite-customer) |
