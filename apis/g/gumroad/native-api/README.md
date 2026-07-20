# Gumroad: Native API Reference

A consolidated summary of Gumroad's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://gumroad.com/api
- **API base URL:** `https://api.gumroad.com/v2`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://gumroad.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.gumroad.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `view_profile edit_products view_sales view_payouts mark_sales_as_shipped edit_sales`.

[Official authentication documentation](https://gumroad.com/help/article/280-create-application-api)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Response data is read from `products`.

## Pagination

Use `page_key` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Custom Field](actions/create-custom-field.md) | `POST /products/:product_id/custom_fields` | [docs](https://gumroad.com/api#post-/products/:product_id/custom_fields) |
| [Create Offer Code](actions/create-offer-code.md) | `POST /products/:product_id/offer_codes` | [docs](https://gumroad.com/api#post-/products/:product_id/offer_codes) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /products/:product_id/custom_fields/:name` | [docs](https://gumroad.com/api#delete-/products/:product_id/custom_fields/:name) |
| [Delete Offer Code](actions/delete-offer-code.md) | `DELETE /products/:product_id/offer_codes/:id` | [docs](https://gumroad.com/api#delete-/products/:product_id/offer_codes/:id) |
| [Disable Product](actions/disable-product.md) | `PUT /products/:id/disable` | [docs](https://gumroad.com/api#put-/products/:id/disable) |
| [Enable Product](actions/enable-product.md) | `PUT /products/:id/enable` | [docs](https://gumroad.com/api#put-/products/:id/enable) |
| [Get Offer Code](actions/get-offer-code.md) | `GET /products/:product_id/offer_codes/:id` | [docs](https://gumroad.com/api#get-/products/:product_id/offer_codes/:id) |
| [Get Payout](actions/get-payout.md) | `GET /payouts/:id` | [docs](https://gumroad.com/api#get-/payouts/:id) |
| [Get Product](actions/get-product.md) | `GET /products/:id` | [docs](https://gumroad.com/api#get-/products/:id) |
| [Get Sale](actions/get-sale.md) | `GET /sales/:id` | [docs](https://gumroad.com/api#get-/sales/:id) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /subscribers/:id` | [docs](https://gumroad.com/api#get-/subscribers/:id) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://gumroad.com/api#get-/user) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /products/:product_id/custom_fields` | [docs](https://gumroad.com/api#get-/products/:product_id/custom_fields) |
| [List Offer Codes](actions/list-offer-codes.md) | `GET /products/:product_id/offer_codes` | [docs](https://gumroad.com/api#get-/products/:product_id/offer_codes) |
| [List Payouts](actions/list-payouts.md) | `GET /payouts` | [docs](https://gumroad.com/api#get-/payouts) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://gumroad.com/api#get-/products) |
| [List Sales](actions/list-sales.md) | `GET /sales` | [docs](https://gumroad.com/api#get-/sales) |
| [List Subscribers](actions/list-subscribers.md) | `GET /products/:product_id/subscribers` | [docs](https://gumroad.com/api#get-/products/:product_id/subscribers) |
| [List Upcoming Payouts](actions/list-upcoming-payouts.md) | `GET /payouts/upcoming` | [docs](https://gumroad.com/api#get-/payouts/upcoming) |
| [Mark Sale as Shipped](actions/mark-sale-as-shipped.md) | `PUT /sales/:id/mark_as_shipped` | [docs](https://gumroad.com/api#put-/sales/:id/mark_as_shipped) |
| [Refund Sale](actions/refund-sale.md) | `PUT /sales/:id/refund` | [docs](https://gumroad.com/api#put-/sales/:id/refund) |
| [Resend Sale Receipt](actions/resend-sale-receipt.md) | `POST /sales/:id/resend_receipt` | [docs](https://gumroad.com/api#post-/sales/:id/resend_receipt) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /products/:product_id/custom_fields/:name` | [docs](https://gumroad.com/api#put-/products/:product_id/custom_fields/:name) |
| [Update Offer Code](actions/update-offer-code.md) | `PUT /products/:product_id/offer_codes/:id` | [docs](https://gumroad.com/api#put-/products/:product_id/offer_codes/:id) |
