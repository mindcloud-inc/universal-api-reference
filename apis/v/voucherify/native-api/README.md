# Voucherify: Native API Reference

A consolidated summary of Voucherify's API configuration and 51 documented operations, with links to official documentation.

- **Official docs:** https://docs.voucherify.io/api-reference
- **API base URL:** `https://us1.api.voucherify.io/v1`

## Authentication

### Voucherify Custom Auth

Use the exact Voucherify header contract with X-App-Id, X-App-Token, and an optional X-Voucherify-Channel value.

### Credentials

- **App ID:** `appId` · required · Voucherify X-App-Id header value.
- **App Token:** `appToken` · required · Voucherify X-App-Token header value.
- **Channel:** `channel` · optional · Optional X-Voucherify-Channel header value for request context.

Send these headers with each API request:

```http
X-App-Id: <appId>
X-App-Token: <appToken>
X-Voucherify-Channel: <channel>
```

[Official authentication documentation](https://docs.voucherify.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (51 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | `POST /categories` | [docs](https://docs.voucherify.io/api-reference/categories) |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://docs.voucherify.io/reference/create-customer) |
| [Create Export](actions/create-export.md) | `POST /exports` | [docs](https://docs.voucherify.io/api-reference/exports) |
| [Create Product](actions/create-product.md) | `POST /products` | [docs](https://docs.voucherify.io/reference/create-product) |
| [Create Publication](actions/create-publication.md) | `POST /publications` | [docs](https://docs.voucherify.io/api-reference/publications) |
| [Create Redemption](actions/create-redemption.md) | `POST /redemptions` | [docs](https://docs.voucherify.io/api-reference/redemptions) |
| [Create Voucher](actions/create-voucher.md) | `POST /vouchers` | [docs](https://docs.voucherify.io/api-reference/vouchers) |
| [Delete Category](actions/delete-category.md) | `DELETE /categories/:categoryId` | [docs](https://docs.voucherify.io/api-reference/categories) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /customers/:customerId` | [docs](https://docs.voucherify.io/reference/delete-customer) |
| [Delete Product](actions/delete-product.md) | `DELETE /products/:productId` | [docs](https://docs.voucherify.io/reference/delete-product) |
| [Delete Voucher](actions/delete-voucher.md) | `DELETE /vouchers/:voucherId` | [docs](https://docs.voucherify.io/api-reference/vouchers) |
| [Get Async Action](actions/get-async-action.md) | `GET /async-actions/:asyncActionId` | [docs](https://docs.voucherify.io/api-reference/async-actions) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://docs.voucherify.io/reference/get-campaign) |
| [Get Category](actions/get-category.md) | `GET /categories/:categoryId` | [docs](https://docs.voucherify.io/reference/get-category) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:customerId` | [docs](https://docs.voucherify.io/reference/get-customer) |
| [Get Export](actions/get-export.md) | `GET /exports/:exportId` | [docs](https://docs.voucherify.io/api-reference/exports) |
| [Get Metadata Schema](actions/get-metadata-schema.md) | `GET /metadata-schemas/:relatedObject` | [docs](https://docs.voucherify.io/api-reference/metadata-schemas) |
| [Get Order](actions/get-order.md) | `GET /orders/:orderId` | [docs](https://docs.voucherify.io/reference/get-order) |
| [Get Product](actions/get-product.md) | `GET /products/:productId` | [docs](https://docs.voucherify.io/reference/get-product) |
| [Get Product Collection](actions/get-product-collection.md) | `GET /product-collections/:collectionId` | [docs](https://docs.voucherify.io/reference/get-product-collection) |
| [Get Publication](actions/get-publication.md) | `GET /publications/:publicationId` | [docs](https://docs.voucherify.io/reference/get-publication) |
| [Get Redemption](actions/get-redemption.md) | `GET /redemptions/:redemptionId` | [docs](https://docs.voucherify.io/reference/get-redemption) |
| [Get Reward](actions/get-reward.md) | `GET /rewards/:rewardId` | [docs](https://docs.voucherify.io/api-reference/rewards) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:segmentId` | [docs](https://docs.voucherify.io/reference/get-segment) |
| [Get Validation Rule](actions/get-validation-rule.md) | `GET /validation-rules/:validationRuleId` | [docs](https://docs.voucherify.io/api-reference/validation-rules) |
| [Get Validation Rule Assignment](actions/get-validation-rule-assignment.md) | `GET /validation-rules-assignments/:assignmentId` | [docs](https://docs.voucherify.io/reference/get-validation-rule-assignment) |
| [Get Voucher](actions/get-voucher.md) | `GET /vouchers/:voucherId` | [docs](https://docs.voucherify.io/reference/get-voucher) |
| [List Async Actions](actions/list-async-actions.md) | `GET /async-actions` | [docs](https://docs.voucherify.io/api-reference/async-actions) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://docs.voucherify.io/reference/list-campaigns) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://docs.voucherify.io/reference/list-categories) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://docs.voucherify.io/reference/list-customers) |
| [List Exports](actions/list-exports.md) | `GET /exports` | [docs](https://docs.voucherify.io/api-reference/exports) |
| [List Loyalty Campaigns](actions/list-loyalty-campaigns.md) | `GET /loyalties` | [docs](https://docs.voucherify.io/reference/list-loyalties) |
| [List Metadata Schemas](actions/list-metadata-schemas.md) | `GET /metadata-schemas` | [docs](https://docs.voucherify.io/api-reference/metadata-schemas) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://docs.voucherify.io/reference/list-orders) |
| [List Product Collections](actions/list-product-collections.md) | `GET /product-collections` | [docs](https://docs.voucherify.io/reference/list-product-collections) |
| [List Products](actions/list-products.md) | `GET /products` | [docs](https://docs.voucherify.io/reference/list-products) |
| [List Publications](actions/list-publications.md) | `GET /publications` | [docs](https://docs.voucherify.io/reference/list-publications) |
| [List Redemptions](actions/list-redemptions.md) | `GET /redemptions` | [docs](https://docs.voucherify.io/reference/list-redemptions) |
| [List Rewards](actions/list-rewards.md) | `GET /rewards` | [docs](https://docs.voucherify.io/api-reference/rewards) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://docs.voucherify.io/reference/list-segments) |
| [List Validation Rule Assignments](actions/list-validation-rule-assignments.md) | `GET /validation-rules-assignments` | [docs](https://docs.voucherify.io/reference/list-validation-rule-assignments) |
| [List Validation Rules](actions/list-validation-rules.md) | `GET /validation-rules` | [docs](https://docs.voucherify.io/api-reference/validation-rules) |
| [List Voucher Publications](actions/list-voucher-publications.md) | `GET /vouchers/:voucherId/publications` | [docs](https://docs.voucherify.io/api-reference/vouchers) |
| [List Voucher Redemptions](actions/list-voucher-redemptions.md) | `GET /vouchers/:voucherId/redemptions` | [docs](https://docs.voucherify.io/api-reference/vouchers) |
| [List Voucher Transactions](actions/list-voucher-transactions.md) | `GET /vouchers/:voucherId/transactions` | [docs](https://docs.voucherify.io/api-reference/vouchers/list-voucher-transactions) |
| [List Vouchers](actions/list-vouchers.md) | `GET /vouchers` | [docs](https://docs.voucherify.io/reference/list-vouchers) |
| [Update Category](actions/update-category.md) | `PUT /categories/:categoryId` | [docs](https://docs.voucherify.io/api-reference/categories) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customerId` | [docs](https://docs.voucherify.io/reference/update-customer) |
| [Update Product](actions/update-product.md) | `PUT /products/:productId` | [docs](https://docs.voucherify.io/reference/update-product) |
| [Update Voucher](actions/update-voucher.md) | `PUT /vouchers/:voucherId` | [docs](https://docs.voucherify.io/api-reference/vouchers) |
