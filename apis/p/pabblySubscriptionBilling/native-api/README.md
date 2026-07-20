# Pabbly Subscription Billing: Native API Reference

A consolidated summary of Pabbly Subscription Billing's API configuration and 88 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.pabbly.com/
- **API base URL:** `https://payments.pabbly.com/api`

## Authentication

### Basic Auth

Pabbly Subscription Billing uses Basic Auth with the API Key as the username and the Secret Key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.pabbly.com/subscriptions/docs/getting-started-guide/)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (88 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Credit](actions/add-credit.md) | `POST /v1/subscription/credit/:subscriptionId/create` | [docs](https://apidocs.pabbly.com/#7aebc903-0491-4b53-bf8b-2100eaa1d994) |
| [Affiliate Clicks](actions/affiliate-clicks.md) | `GET /v1/commissions/clicks` | [docs](https://apidocs.pabbly.com/#475cec17-11a8-4df8-98ac-6aab9f51198d) |
| [Affiliate Links](actions/affiliate-links.md) | `GET /v1/affiliate/links` | [docs](https://apidocs.pabbly.com/#03175ff7-5f78-4993-b749-79567cc5cb29) |
| [Cancel Subscription For Existing Customer](actions/cancel-subscription-for-existing-customer.md) | `POST /v1/subscription/:subscriptionId/cancel` | [docs](https://apidocs.pabbly.com/#86de662e-d6ef-4a8b-a35f-a37c8b2f880e) |
| [Change Subscription Billing Date](actions/change-subscription-billing-date.md) | `PUT /v1/subscription/change-billing/:subscriptionId` | [docs](https://apidocs.pabbly.com/#37492ea6-99bc-4b8e-81eb-8c7165a86eca) |
| [Create Addon](actions/create-addon.md) | `POST /v1/addon/:productId` | [docs](https://apidocs.pabbly.com/#225afde3-a358-48ec-a8c7-33da68a98ae6) |
| [Create Addon Category](actions/create-addon-category.md) | `POST /v1/addoncategory` | [docs](https://apidocs.pabbly.com/#0d52cc27-d0b8-43e6-b9e8-d5c3df28d687) |
| [Create Client Portal API Session](actions/create-client-portal-api-session.md) | `POST /v1/portal_sessions` | [docs](https://apidocs.pabbly.com/#4ce484dc-3bf7-4bac-9eac-5c89a51d64be) |
| [Create Commission](actions/create-commission.md) | `POST /v1/commissions/create` | [docs](https://apidocs.pabbly.com/#eee0a320-9e4e-4225-9da6-feef8a22a25f) |
| [Create Commission Rule](actions/create-commission-rule.md) | `POST /v1/affiliate/commissionrule/create` | [docs](https://apidocs.pabbly.com/#996aa738-a1f0-437a-90fb-901350c1f3f5) |
| [Create Coupon](actions/create-coupon.md) | `POST /v1/coupon/:productId` | [docs](https://apidocs.pabbly.com/#423ee687-4e13-45a1-8b55-4be1ea86a47c) |
| [Create Customer](actions/create-customer.md) | `POST /v1/customer` | [docs](https://apidocs.pabbly.com/#cde44e73-4f9d-44bc-be76-358c3a1633d7) |
| [Create Customer With Subscription](actions/create-customer-with-subscription.md) | `POST /v1/subscription` | [docs](https://apidocs.pabbly.com/#fa365f13-a67c-4973-8967-0e4db2c2a109) |
| [Create License](actions/create-license.md) | `POST /v1/products/:productId/licenses` | [docs](https://apidocs.pabbly.com/#ce7e52a1-d4d7-4583-bca2-48eee6ddc95d) |
| [Create Manual Report](actions/create-manual-report.md) | `POST /v1/affiliate/payout/generate` | [docs](https://apidocs.pabbly.com/#8fabbce8-b48b-4979-a7e6-1f6f6018e101) |
| [Create Metered Invoice](actions/create-metered-invoice.md) | `POST /v1/invoices/create-metered/:subscriptionId` | [docs](https://apidocs.pabbly.com/#bbd62eae-1f32-4e94-8284-7c4e005de6dd) |
| [Create Monthly Recurring Revenue Status](actions/create-monthly-recurring-revenue-status.md) | `POST /v1/mrrsubscription` | [docs](https://apidocs.pabbly.com/#193ca50e-a971-4436-86af-c091651cc31f) |
| [Create Net-Revenue Status](actions/create-net-revenue-status.md) | `POST /v1/revenuetransaction` | [docs](https://apidocs.pabbly.com/#3b04f8ad-a6fc-41d7-bf45-2363fd3dd593) |
| [Create Payment Method](actions/create-payment-method.md) | `POST /v1/paymentmethod/:customerId` | [docs](https://apidocs.pabbly.com/#120f63aa-80f5-44e1-86c4-7d38ac07ed0a) |
| [Create Plan](actions/create-plan.md) | `POST /v1/plan/create` | [docs](https://apidocs.pabbly.com/#039094b9-417b-4f79-9f6e-baa9fcf95074) |
| [Create Product](actions/create-product.md) | `POST /v1/product/create` | [docs](https://apidocs.pabbly.com/#f06933f1-0a3f-4a49-94af-52a830cc6c28) |
| [Create Subscription For Existing Customer](actions/create-subscription-for-existing-customer.md) | `POST /v1/subscription/:customerId` | [docs](https://apidocs.pabbly.com/#6143db10-efd1-42f9-91da-0ced427e871f) |
| [Dashboard Stats](actions/dashboard-stats.md) | `POST /v2/getdashboardstats` | [docs](https://apidocs.pabbly.com/#754ecd31-59d3-4106-a4f4-47d820a317c1) |
| [Deduct Credit](actions/deduct-credit.md) | `POST /v1/subscription/credit/:subscriptionId/deduct` | [docs](https://apidocs.pabbly.com/#6c0f8f80-d52c-4a52-8ea7-9b0788e2c93b) |
| [Delete Addon](actions/delete-addon.md) | `DELETE /v1/addon/:addonId` | [docs](https://apidocs.pabbly.com/#bd56a17a-8c95-49f0-b54a-2c61dad59804) |
| [Delete Addon Category](actions/delete-addon-category.md) | `DELETE /v1/addoncategory/:categoryId` | [docs](https://apidocs.pabbly.com/#e53e9ad6-bbb2-4851-bac4-9df25f321095) |
| [Delete Clicks](actions/delete-clicks.md) | `DELETE /v1/commissions/clicks/:clickId` | [docs](https://apidocs.pabbly.com/#7ddf5122-c672-47c9-bc99-03f52ba3ba1f) |
| [Delete Coupon](actions/delete-coupon.md) | `DELETE /v1/coupons/:couponId` | [docs](https://apidocs.pabbly.com/#6662d924-a4b6-41ca-a391-de02b35ea31d) |
| [Delete Customer](actions/delete-customer.md) | `DELETE /v1/customers/:customerId` | [docs](https://apidocs.pabbly.com/#edc684f5-8b07-4bf2-934f-28bcc81f7fdb) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE /v1/invoices/:invoiceId` | [docs](https://apidocs.pabbly.com/#6109fd39-577d-4a99-bbf2-d0d276e30656) |
| [Delete License](actions/delete-license.md) | `DELETE /v1/products/:productId/licenses/:licenseId` | [docs](https://apidocs.pabbly.com/#2d06cb1a-a683-42af-99e5-f7e6b1d4ba9c) |
| [Delete License Code](actions/delete-license-code.md) | `DELETE /v1/products/:productId/licenses/:licenseId/codes/:code` | [docs](https://apidocs.pabbly.com/#994224d4-cc6d-4a1a-8abe-9c8526ab860f) |
| [Delete Plan](actions/delete-plan.md) | `DELETE /v1/plans/:planId` | [docs](https://apidocs.pabbly.com/#e3e73cb2-80e3-42c6-bdcd-b1cb8a0483fc) |
| [Delete Product](actions/delete-product.md) | `DELETE /v1/products/:productId` | [docs](https://apidocs.pabbly.com/#3dadd4ac-321e-427d-b384-ef37c498df5c) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /v1/subscriptions/:subscriptionId` | [docs](https://apidocs.pabbly.com/#e601bb11-8b0f-4bf2-9bbf-83e3b24691af) |
| [Delete Transaction](actions/delete-transaction.md) | `DELETE /v1/transaction/:transactionId` | [docs](https://apidocs.pabbly.com/#7ac6cab1-4713-4c32-8932-4127afbd3b84) |
| [Get Add Card URL](actions/get-add-card-url.md) | `GET /v1/add_card_url/:customerId` | [docs](https://apidocs.pabbly.com/#e2d107db-2b3e-4738-8f33-04940ba7abf0) |
| [Get Checkout Page By Product Id](actions/get-checkout-page-by-product-id.md) | `GET /v1/checkoutpage/:productId` | [docs](https://apidocs.pabbly.com/#0fd2973c-00b0-484c-8624-854149f2eb4a) |
| [Get Custom Fields](actions/get-custom-fields.md) | `GET /v1/customfields/:planId` | [docs](https://apidocs.pabbly.com/#c704c30a-3170-4351-a281-a5eb6ec42b9d) |
| [Get Customer Purchase Information](actions/get-customer-purchase-information.md) | `GET /v1/customer/purchase-info/:customerId` | [docs](https://apidocs.pabbly.com/#7eceef52-adfc-48a1-9a3f-8c1971f5e024) |
| [Get Hosted Page Data](actions/get-hosted-page-data.md) | `GET /v1/hostedpage` | [docs](https://apidocs.pabbly.com/#94797e1a-5325-44eb-bdfb-597332a7a8c1) |
| [Get License Codes](actions/get-license-codes.md) | `GET /v1/products/:productId/licenses/:licenseId/codes` | [docs](https://apidocs.pabbly.com/#49bd15f3-baf4-4e4f-8590-1ef0d4f0d3e2) |
| [Get Multiplan Details](actions/get-multiplan-details.md) | `GET /v1/multiplans/:multiplanId` | [docs](https://apidocs.pabbly.com/#2adad39c-837e-49b9-8155-685e922ff0e4) |
| [Get Scheduled Subscription](actions/get-scheduled-subscription.md) | `GET /v1/scheduledchanges/:subscriptionId` | [docs](https://apidocs.pabbly.com/#b63826e4-4328-457b-b450-c5b7cb53d43d) |
| [Get Single Addon](actions/get-single-addon.md) | `GET /v1/addon/:addonId` | [docs](https://apidocs.pabbly.com/#5059cd08-702f-4e6c-8022-cd2ef3e0bfd2) |
| [Get Single Addon Category](actions/get-single-addon-category.md) | `GET /v1/addoncategory/:addonId` | [docs](https://apidocs.pabbly.com/#743063b4-4e4b-4568-9f72-8b525f7d5117) |
| [Get Single Customer via Customer Email](actions/get-single-customer-via-customer-email.md) | `GET /v1/customer` | [docs](https://apidocs.pabbly.com/#898d4498-51ed-43aa-8f10-ee73addfa255) |
| [Get Single Customer via Customer ID](actions/get-single-customer-via-customer-id.md) | `GET /v1/customer/:customerId` | [docs](https://apidocs.pabbly.com/#4ac6de74-d5dc-4ea6-89eb-b00fd52a05b8) |
| [Get Single Invoice](actions/get-single-invoice.md) | `GET /v1/invoice/:invoiceId` | [docs](https://apidocs.pabbly.com/#41d4bb31-a125-4f1d-9bcd-fbe2bc95ff4c) |
| [Get Single License](actions/get-single-license.md) | `GET /v1/products/:productId/licenses/:licenseId` | [docs](https://apidocs.pabbly.com/#40466acc-c620-446b-b8a3-501bc4b23c7f) |
| [Get single Plan by Plan ID](actions/get-single-plan-by-plan-id.md) | `GET /v1/plan/:planId` | [docs](https://apidocs.pabbly.com/#8e78c6df-2503-41bd-84db-6921730d5e4f) |
| [Get Single Product By Product ID](actions/get-single-product-by-product-id.md) | `GET /v1/product/:productId` | [docs](https://apidocs.pabbly.com/#cac7156f-c102-4cc0-a40f-95f890a6572e) |
| [Get Single Subscription](actions/get-single-subscription.md) | `GET /v1/subscription/:subscriptionId` | [docs](https://apidocs.pabbly.com/#98302eb8-a3ff-4cd2-99ea-8c77fd27dbe7) |
| [List All Addon Categories By Product ID](actions/list-all-addon-categories-by-product-id.md) | `GET /v1/addonlistcategory/:productId` | [docs](https://apidocs.pabbly.com/#3a7f9c57-7ef5-4d34-8920-f7bdf7f71489) |
| [List All Addons](actions/list-all-addons.md) | `GET /v1/addons/:productId` | [docs](https://apidocs.pabbly.com/#03ea0f12-3f1b-4f56-b95d-a0aa46fd04e0) |
| [List All Coupons By Product](actions/list-all-coupons-by-product.md) | `GET /v1/coupon/:productId` | [docs](https://apidocs.pabbly.com/#c5c5010c-104b-4c7c-bbad-7da44f37c787) |
| [List All Customers](actions/list-all-customers.md) | `GET /v1/customers` | [docs](https://apidocs.pabbly.com/#4a13736a-509e-4347-b5e6-988fbae8e194) |
| [List All Invoices](actions/list-all-invoices.md) | `GET /v1/invoices` | [docs](https://apidocs.pabbly.com/#30ee5ad3-c165-4bb9-a60f-88eadff66acd) |
| [List All Invoices By Customer Id](actions/list-all-invoices-by-customer-id.md) | `GET /v1/invoices/:customerId` | [docs](https://apidocs.pabbly.com/#89d50c1d-52e1-4479-b56b-0689b11ec867) |
| [List All Licenses](actions/list-all-licenses.md) | `GET /v1/products/:productId/licenses` | [docs](https://apidocs.pabbly.com/#59ba8d92-ae2c-4e50-8b84-67bca4938e01) |
| [List All Multiplans](actions/list-all-multiplans.md) | `GET /v1/multiplans` | [docs](https://apidocs.pabbly.com/#06bf21a5-a752-4ab1-a73e-8fe2164fe526) |
| [List All Payment Gateways](actions/list-all-payment-gateways.md) | `GET /v1/paymentgateways` | [docs](https://apidocs.pabbly.com/#0a9b6292-1fe1-457e-a634-1f4451319b64) |
| [List All Payment Methods By Customer Id](actions/list-all-payment-methods-by-customer-id.md) | `GET /v1/paymentmethods/:customerId` | [docs](https://apidocs.pabbly.com/#771ac2ca-ad84-4eb8-9fae-9a493d53a44c) |
| [List All Plans](actions/list-all-plans.md) | `GET /v1/plans` | [docs](https://apidocs.pabbly.com/#f3e850a9-c16a-472e-a870-9ae954d81524) |
| [List All Plans By Product ID](actions/list-all-plans-by-product-id.md) | `GET /v1/plans/:productId` | [docs](https://apidocs.pabbly.com/#b171036f-4c16-4de2-8ab2-6b5e09078145) |
| [List All Product](actions/list-all-product.md) | `GET /v1/products` | [docs](https://apidocs.pabbly.com/#dc18495d-ac7c-489c-a590-dd7035d523c1) |
| [List All Refund By Customer Id](actions/list-all-refund-by-customer-id.md) | `GET /v1/refund/:customerId` | [docs](https://apidocs.pabbly.com/#f6e74481-c273-4337-ac16-17ed5b233d61) |
| [List All Subscriptions](actions/list-all-subscriptions.md) | `GET /v1/subscriptions` | [docs](https://apidocs.pabbly.com/#30d9b403-4bc2-49de-bdf8-b4147a55fb5c) |
| [List All Subscriptions By Customer Id](actions/list-all-subscriptions-by-customer-id.md) | `GET /v1/subscriptions/:customerId` | [docs](https://apidocs.pabbly.com/#cfd67f09-fea5-45ea-939e-7d10987806a1) |
| [List All Transactions By Customer Id](actions/list-all-transactions-by-customer-id.md) | `GET /v1/transactions/:customerId` | [docs](https://apidocs.pabbly.com/#ee9ef738-1a1c-4a3f-a036-8b22b9a3c48a) |
| [List All Transactions By Invoice Id](actions/list-all-transactions-by-invoice-id.md) | `GET /v1/invoices/transactions/:invoiceId` | [docs](https://apidocs.pabbly.com/#a80c6515-92a8-44bd-8b25-8bcce09cce99) |
| [List Commissions](actions/list-commissions.md) | `GET /v1/commissions` | [docs](https://apidocs.pabbly.com/#2e4213fb-1341-479d-8f5d-cfdaec1df51f) |
| [Payment Refund](actions/payment-refund.md) | `POST /v1/transaction/refund/:paymentId` | [docs](https://apidocs.pabbly.com/#0b37e2f9-1dfb-4bc7-8de9-29f770e7a2a4) |
| [Record Failed Payment Invoice](actions/record-failed-payment-invoice.md) | `POST /v1/invoice/failedpayment/:invoiceId` | [docs](https://apidocs.pabbly.com/#39077735-919c-48b0-aa66-ffb6663644d2) |
| [Record Payment Invoice](actions/record-payment-invoice.md) | `POST /v1/invoice/recordpayment/:invoiceId` | [docs](https://apidocs.pabbly.com/#115d662a-41b2-447a-a984-604bb5675e1c) |
| [Record Refund](actions/record-refund.md) | `POST /v1/transaction/refund/:paymentId` | [docs](https://apidocs.pabbly.com/#7077d374-cd40-43da-ad83-0904dde1ecdc) |
| [Subscription Update Charges](actions/subscription-update-charges.md) | `POST /v1/subscription/:subscriptionId/update_charges` | [docs](https://apidocs.pabbly.com/#91017921-1880-4c11-ae56-e728dff46d44) |
| [Update Addon](actions/update-addon.md) | `PUT /v1/addon/:addonId` | [docs](https://apidocs.pabbly.com/#720877c8-8638-4e36-a73e-ad4f5e6816ec) |
| [Update Addon Category](actions/update-addon-category.md) | `PUT /v1/addoncategory/:categoryId` | [docs](https://apidocs.pabbly.com/#0a2fa6ac-6323-4c69-a553-67eeb97343e0) |
| [Update Commission](actions/update-commission.md) | `PUT /v1/commissions/:commissionId` | [docs](https://apidocs.pabbly.com/#60ada6fa-2328-4b50-b86f-206d9c017c76) |
| [Update Custom Fields to Subscription](actions/update-custom-fields-to-subscription.md) | `PUT /v1/subscription/custom-fields/:subscriptionId` | [docs](https://apidocs.pabbly.com/#b5cbe517-9e6b-4ad9-900b-a42f5af94b47) |
| [Update Customer Detail](actions/update-customer-detail.md) | `PUT /v1/customer/:customerId` | [docs](https://apidocs.pabbly.com/#5642ea4b-3e4f-4305-9031-ca7d4f563131) |
| [Update License](actions/update-license.md) | `PUT /v1/products/:productId/licenses/:licenseId` | [docs](https://apidocs.pabbly.com/#7c86256a-3708-4d9c-8042-e57090080e8e) |
| [Update Payment Method For Existing Customer](actions/update-payment-method-for-existing-customer.md) | `PUT /v1/paymentmethod/:customerId` | [docs](https://apidocs.pabbly.com/#343b5646-ed9f-4a45-8032-727e49ea3503) |
| [Update Plan](actions/update-plan.md) | `PUT /v1/plan/update/:planId` | [docs](https://apidocs.pabbly.com/#44a4f878-2940-4284-8bd5-3464d2848298) |
| [Update Product](actions/update-product.md) | `PUT /v1/product/update/:productId` | [docs](https://apidocs.pabbly.com/#a422de7b-b4db-44f3-ae53-ef05414cbacb) |
| [Update Subscription](actions/update-subscription.md) | `PUT /v1/subscription/:subscriptionId/update` | [docs](https://apidocs.pabbly.com/#7f183e52-2085-4f9b-8abd-26ba39fe12d8) |
| [Upgrade Downgrade Subscription](actions/upgrade-downgrade-subscription.md) | `PUT /v1/subscription/:subscriptionId/upgrade-downgrade` | [docs](https://apidocs.pabbly.com/#f38eb77a-8284-4847-b8c0-debbda138399) |
