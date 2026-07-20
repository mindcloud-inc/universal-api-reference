# Lightfunnels: Native API Reference

A consolidated summary of Lightfunnels's API configuration and 63 documented operations, with links to official documentation.

- **Official docs:** https://developer.lightfunnels.com/
- **API base URL:** `https://services.lightfunnels.com`

## Authentication

### OAuth 2.0

Connect a Lightfunnels workspace through the official OAuth2 consent flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.lightfunnels.com/admin/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://api.lightfunnels.com/api/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `funnels,orders,products,analytics,customers,discounts,contact_form_data,settings`.

[Official authentication documentation](https://developer.lightfunnels.com/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (63 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Products to Store](actions/add-products-to-store.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
| [Cancel Order](actions/cancel-order.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/orders) |
| [Create App Charge](actions/create-app-charge.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/app-charges) |
| [Create Bundle](actions/create-bundle.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/bundles) |
| [Create Collection](actions/create-collection.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/collections) |
| [Create Customer](actions/create-customer.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/customers) |
| [Create Discount](actions/create-discount.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/discounts) |
| [Create Facebook Conversion API Integration](actions/create-facebook-conversion-api-integration.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/settings) |
| [Create Funnel](actions/create-funnel.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/funnels) |
| [Create Product](actions/create-product.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/products) |
| [Create Review](actions/create-review.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/reviews) |
| [Create Segment](actions/create-segment.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/segments) |
| [Create Shipping Rate Group](actions/create-shipping-rate-group.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/shipping-rate-groups) |
| [Create Store](actions/create-store.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/webhooks) |
| [Delete Bundle](actions/delete-bundle.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/bundles) |
| [Delete Collection](actions/delete-collection.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/collections) |
| [Delete Discount](actions/delete-discount.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/discounts) |
| [Delete Funnel](actions/delete-funnel.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/funnels) |
| [Delete Products](actions/delete-products.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/products) |
| [Delete Review](actions/delete-review.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/reviews) |
| [Delete Segment](actions/delete-segment.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/segments) |
| [Delete Shipping Rate Group](actions/delete-shipping-rate-group.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/shipping-rate-groups) |
| [Delete Store](actions/delete-store.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
| [Delete Webhook](actions/delete-webhook.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/webhooks) |
| [Get App Charge](actions/get-app-charge.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/app-charges) |
| [Get Bundle](actions/get-bundle.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/bundles) |
| [Get Collection](actions/get-collection.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/collections) |
| [Get Customer](actions/get-customer.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/customers) |
| [Get Discount](actions/get-discount.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/discounts) |
| [Get Funnel](actions/get-funnel.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/funnels) |
| [Get Order](actions/get-order.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/orders) |
| [Get Product](actions/get-product.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/products) |
| [Get Review](actions/get-review.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/reviews) |
| [Get Segment](actions/get-segment.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/segments) |
| [Get Store](actions/get-store.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
| [List App Charges](actions/list-app-charges.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/app-charges) |
| [List Bundles](actions/list-bundles.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/bundles) |
| [List Collections](actions/list-collections.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/collections) |
| [List Customers](actions/list-customers.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/customers) |
| [List Discounts](actions/list-discounts.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/discounts) |
| [List Funnels](actions/list-funnels.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/funnels) |
| [List Orders](actions/list-orders.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/orders) |
| [List Products](actions/list-products.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/products) |
| [List Reviews](actions/list-reviews.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/reviews) |
| [List Segments](actions/list-segments.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/segments) |
| [List Shipping Rate Groups](actions/list-shipping-rate-groups.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/shipping-rate-groups) |
| [List Stores](actions/list-stores.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
| [Remove Integration](actions/remove-integration.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/settings) |
| [Retrieve Account Pixels](actions/retrieve-account-pixels.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/settings) |
| [Retrieve Integrations](actions/retrieve-integrations.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/settings) |
| [Update Account Pixels](actions/update-account-pixels.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/settings) |
| [Update Bundle](actions/update-bundle.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/bundles) |
| [Update Collection](actions/update-collection.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/collections) |
| [Update Customer](actions/update-customer.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/customers) |
| [Update Discount](actions/update-discount.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/discounts) |
| [Update Funnel](actions/update-funnel.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/funnels) |
| [Update Order](actions/update-order.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/orders) |
| [Update Product](actions/update-product.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/products) |
| [Update Review](actions/update-review.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/reviews) |
| [Update Segment](actions/update-segment.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/segments) |
| [Update Shipping Rate Group](actions/update-shipping-rate-group.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/shipping-rate-groups) |
| [Update Store](actions/update-store.md) | `POST /api/v2` | [docs](https://developer.lightfunnels.com/stores) |
