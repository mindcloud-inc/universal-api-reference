# Eduzz: Native API Reference

A consolidated summary of Eduzz's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://developers.eduzz.com/docs/api
- **OpenAPI specification:** https://developers.eduzz.com/api/openapi
- **API base URL:** `https://api.eduzz.com`

## Authentication

### OAuth2

Connect Eduzz with OAuth2 user authorization.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.eduzz.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts-api.eduzz.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://developers.eduzz.com/docs/api/user-token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `itemsPerPage` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Checkout Cart](actions/create-checkout-cart.md) | `POST /sun/v1/cart` | [docs](https://developers.eduzz.com/reference/api/post-sun-v1-cart) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhook/v1/subscription` | [docs](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhook/v1/subscription/:id` | [docs](https://developers.eduzz.com/reference/api/delete-webhook-v1-subscription-id) |
| [Get Account Profile](actions/get-account-profile.md) | `GET /accounts/v1/me` | [docs](https://developers.eduzz.com/reference/api/get-accounts-v1-me) |
| [Get Customer Details by Email](actions/get-customer-details-by-email.md) | `GET /myeduzz/v1/subscriptions/customers/:email` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-subscriptions-customers-email) |
| [Get Financial Statement](actions/get-financial-statement.md) | `GET /myeduzz/v2/financial/statement` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v2-financial-statement) |
| [Get Sales Summary](actions/get-sales-summary.md) | `GET /myeduzz/v1/sales/summary` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales-summary) |
| [Get Webhook Event Sample](actions/get-webhook-event-sample.md) | `GET /webhook/v1/origin/sample/:event` | [docs](https://developers.eduzz.com/reference/api/get-webhook-v1-origin-sample-event) |
| [Get Webhook Secret](actions/get-webhook-secret.md) | `GET /webhook/v1/secret` | [docs](https://developers.eduzz.com/reference/api/get-webhook-v1-secret) |
| [List Affiliates](actions/list-affiliates.md) | `GET /myeduzz/v1/affiliates` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-affiliates) |
| [List Chargebacks](actions/list-chargebacks.md) | `GET /myeduzz/v1/sales/chargebacks` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales-chargebacks) |
| [List Courses](actions/list-courses.md) | `GET /nutror/v1/courses` | [docs](https://developers.eduzz.com/reference/api/get-nutror-v1-courses) |
| [List Customers](actions/list-customers.md) | `GET /myeduzz/v1/customers` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-customers) |
| [List Products](actions/list-products.md) | `GET /myeduzz/v1/products` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-products) |
| [List Sales](actions/list-sales.md) | `GET /myeduzz/v1/sales` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales) |
| [List Students](actions/list-students.md) | `GET /nutror/v1/students` | [docs](https://developers.eduzz.com/reference/api/get-nutror-v1-students) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /myeduzz/v1/subscriptions` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-subscriptions) |
| [List Transfers](actions/list-transfers.md) | `GET /myeduzz/v1/financial/transfers` | [docs](https://developers.eduzz.com/reference/api/get-myeduzz-v1-financial-transfers) |
| [List Webhook Origins](actions/list-webhook-origins.md) | `GET /webhook/v1/origin` | [docs](https://developers.eduzz.com/reference/api/get-webhook-v1-origin) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook/v1/subscription` | [docs](https://developers.eduzz.com/reference/api/get-webhook-v1-subscription) |
| [Request Webhook Test](actions/request-webhook-test.md) | `POST /webhook/v1/subscription/sample` | [docs](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription-sample) |
| [Set Webhook Subscription Status](actions/set-webhook-subscription-status.md) | `POST /webhook/v1/subscription/:id/status` | [docs](https://developers.eduzz.com/reference/api/post-webhook-v1-subscription-id-status) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PUT /webhook/v1/subscription/:subscriptionId` | [docs](https://developers.eduzz.com/reference/api/put-webhook-v1-subscription-subscriptionId) |
