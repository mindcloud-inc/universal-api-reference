# Cheddar: Native API Reference

A consolidated summary of Cheddar's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.getcheddar.com/
- **API base URL:** `https://getcheddar.com/xml`

## Authentication

### Basic Authentication

Use the Cheddar account email as the username and the product secret key/API key as the password for API requests.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Product Code:** `productCode` · required · Required in every Cheddar API path. Copy it from Configuration > Product Settings.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.getcheddar.com/)

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderByDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Charge or Credit](actions/add-custom-charge-or-credit.md) | `POST /customers/add-charge/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#add-a-custom-charge-credit) |
| [Add Item Quantity](actions/add-item-quantity.md) | `POST /customers/add-item-quantity/productCode/{{credentials.productCode}}/code/:customerCode/itemCode/:itemCode` | [docs](https://docs.getcheddar.com/#add-item-quantity) |
| [Cancel Subscription](actions/cancel-subscription.md) | `POST /customers/cancel/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#cancel-a-customer-39-s-subscription) |
| [Create Customer](actions/create-customer.md) | `POST /customers/new/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#create-a-new-customer) |
| [Create One-Time Invoice](actions/create-one-time-invoice.md) | `POST /invoices/new/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#create-a-one-time-invoice) |
| [Delete Custom Charge or Credit](actions/delete-custom-charge-or-credit.md) | `POST /customers/delete-charge/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#delete-a-custom-charge-credit) |
| [Delete Customer](actions/delete-customer.md) | `POST /customers/delete/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#delete-a-customer) |
| [Get Customer](actions/get-customer.md) | `GET /customers/get/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#get-a-single-customer) |
| [Get Pricing Plan](actions/get-pricing-plan.md) | `GET /plans/get/productCode/{{credentials.productCode}}/code/:planCode` | [docs](https://docs.getcheddar.com/#get-a-single-pricing-plan) |
| [Get Promotion](actions/get-promotion.md) | `GET /promotions/get/productCode/{{credentials.productCode}}/code/:promotionCode` | [docs](https://docs.getcheddar.com/#get-a-single-promotions) |
| [Import Customers](actions/import-customers.md) | `POST /customers/import/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#import-customers) |
| [Issue Refund](actions/issue-refund.md) | `POST /invoices/refund/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#issue-a-refund) |
| [Issue Void](actions/issue-void.md) | `POST /invoices/void/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#issue-a-void) |
| [Issue Void or Refund](actions/issue-void-or-refund.md) | `POST /invoices/void-or-refund/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#issue-a-void-or-refund) |
| [List Customers](actions/list-customers.md) | `GET /customers/get/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#get-all-customers) |
| [List Pricing Plans](actions/list-pricing-plans.md) | `GET /plans/get/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#get-all-pricing-plans) |
| [List Promotions](actions/list-promotions.md) | `GET /promotions/get/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#get-all-promotions) |
| [Remove Item Quantity](actions/remove-item-quantity.md) | `POST /customers/remove-item-quantity/productCode/{{credentials.productCode}}/code/:customerCode/itemCode/:itemCode` | [docs](https://docs.getcheddar.com/#remove-item-quantity) |
| [Run Outstanding Invoice](actions/run-outstanding-invoice.md) | `POST /customers/run-outstanding/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#run-an-outstanding-invoice) |
| [Send or Resend Invoice Email](actions/send-or-resend-invoice-email.md) | `POST /invoices/send-email/productCode/{{credentials.productCode}}` | [docs](https://docs.getcheddar.com/#send-or-resend-an-invoice-email) |
| [Set Item Quantity](actions/set-item-quantity.md) | `POST /customers/set-item-quantity/productCode/{{credentials.productCode}}/code/:customerCode/itemCode/:itemCode` | [docs](https://docs.getcheddar.com/#set-item-quantity) |
| [Update Customer](actions/update-customer.md) | `POST /customers/edit-customer/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#update-a-customer-only) |
| [Update Customer and Subscription](actions/update-customer-and-subscription.md) | `POST /customers/edit/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#update-a-customer-and-subscription) |
| [Update Subscription](actions/update-subscription.md) | `POST /customers/edit-subscription/productCode/{{credentials.productCode}}/code/:customerCode` | [docs](https://docs.getcheddar.com/#update-a-subscription-only) |
