# <img src="https://images.mindcloud.co/apps/icons/captura-de-tela-2026-04-20-as-14_1776707945537.png" alt="Pabbly Subscription Billing logo" width="28" height="28"> Pabbly Subscription Billing: Universal API

Manage Pabbly Subscription Billing customers, subscriptions, products, plans, coupons, invoices, payment methods, transactions, refunds, client portal sessions, and payment gateways through Pabbly's REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pabblySubscriptionBilling/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 88
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pabbly.com/subscriptions/
- **Vendor API docs:** https://apidocs.pabbly.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Customers](actions/list-all-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (88)

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Get Checkout Page By Product Id](actions/get-checkout-page-by-product-id.md) | GET |  |
| [Get Hosted Page Data](actions/get-hosted-page-data.md) | GET |  |

### Coupons

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon](actions/create-coupon.md) | POST |  |
| [Delete Coupon](actions/delete-coupon.md) | DELETE |  |
| [List All Coupons By Product](actions/list-all-coupons-by-product.md) | GET |  |

### Credit Notes

| Action | Method | Description |
| --- | --- | --- |
| [Add Credit](actions/add-credit.md) | POST |  |
| [Deduct Credit](actions/deduct-credit.md) | POST |  |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Fields](actions/get-custom-fields.md) | GET |  |
| [Update Custom Fields to Subscription](actions/update-custom-fields-to-subscription.md) | PUT |  |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST |  |
| [Create Customer With Subscription](actions/create-customer-with-subscription.md) | POST |  |
| [Delete Customer](actions/delete-customer.md) | DELETE |  |
| [Get Customer Purchase Information](actions/get-customer-purchase-information.md) | GET |  |
| [Get Single Customer via Customer Email](actions/get-single-customer-via-customer-email.md) | GET |  |
| [Get Single Customer via Customer ID](actions/get-single-customer-via-customer-id.md) | GET |  |
| [List All Customers](actions/list-all-customers.md) | GET |  |
| [Update Customer Detail](actions/update-customer-detail.md) | PUT |  |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Dashboard Stats](actions/dashboard-stats.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Metered Invoice](actions/create-metered-invoice.md) | POST |  |
| [Delete Invoice](actions/delete-invoice.md) | DELETE |  |
| [Get Single Invoice](actions/get-single-invoice.md) | GET |  |
| [List All Invoices](actions/list-all-invoices.md) | GET |  |
| [List All Invoices By Customer Id](actions/list-all-invoices-by-customer-id.md) | GET |  |
| [List All Transactions By Invoice Id](actions/list-all-transactions-by-invoice-id.md) | GET |  |
| [Record Failed Payment Invoice](actions/record-failed-payment-invoice.md) | PUT |  |
| [Record Payment Invoice](actions/record-payment-invoice.md) | PUT |  |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Method](actions/create-payment-method.md) | POST |  |
| [Get Add Card URL](actions/get-add-card-url.md) | GET |  |
| [List All Payment Gateways](actions/list-all-payment-gateways.md) | GET |  |
| [List All Payment Methods By Customer Id](actions/list-all-payment-methods-by-customer-id.md) | GET |  |
| [Update Payment Method For Existing Customer](actions/update-payment-method-for-existing-customer.md) | PUT |  |

### Product Variants

| Action | Method | Description |
| --- | --- | --- |
| [Create Addon](actions/create-addon.md) | POST |  |
| [Create Addon Category](actions/create-addon-category.md) | POST |  |
| [Delete Addon](actions/delete-addon.md) | DELETE |  |
| [Delete Addon Category](actions/delete-addon-category.md) | DELETE |  |
| [Get Single Addon](actions/get-single-addon.md) | GET |  |
| [Get Single Addon Category](actions/get-single-addon-category.md) | GET |  |
| [List All Addon Categories By Product ID](actions/list-all-addon-categories-by-product-id.md) | GET |  |
| [List All Addons](actions/list-all-addons.md) | GET |  |
| [Update Addon](actions/update-addon.md) | PUT |  |
| [Update Addon Category](actions/update-addon-category.md) | PUT |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Delete Product](actions/delete-product.md) | DELETE |  |
| [Get Single Product By Product ID](actions/get-single-product-by-product-id.md) | GET |  |
| [List All Product](actions/list-all-product.md) | GET |  |
| [Update Product](actions/update-product.md) | PUT |  |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [List All Refund By Customer Id](actions/list-all-refund-by-customer-id.md) | GET |  |
| [Payment Refund](actions/payment-refund.md) | POST |  |
| [Record Refund](actions/record-refund.md) | POST |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Create Manual Report](actions/create-manual-report.md) | POST |  |
| [Create Monthly Recurring Revenue Status](actions/create-monthly-recurring-revenue-status.md) | GET |  |
| [Create Net-Revenue Status](actions/create-net-revenue-status.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Client Portal API Session](actions/create-client-portal-api-session.md) | POST |  |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST |  |
| [Delete Plan](actions/delete-plan.md) | DELETE |  |
| [Get Multiplan Details](actions/get-multiplan-details.md) | GET |  |
| [Get single Plan by Plan ID](actions/get-single-plan-by-plan-id.md) | GET |  |
| [List All Multiplans](actions/list-all-multiplans.md) | GET |  |
| [List All Plans](actions/list-all-plans.md) | GET |  |
| [List All Plans By Product ID](actions/list-all-plans-by-product-id.md) | GET |  |
| [Update Plan](actions/update-plan.md) | PUT |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription For Existing Customer](actions/cancel-subscription-for-existing-customer.md) | PUT |  |
| [Change Subscription Billing Date](actions/change-subscription-billing-date.md) | PUT |  |
| [Create Subscription For Existing Customer](actions/create-subscription-for-existing-customer.md) | POST |  |
| [Delete Subscription](actions/delete-subscription.md) | DELETE |  |
| [Get Scheduled Subscription](actions/get-scheduled-subscription.md) | GET |  |
| [Get Single Subscription](actions/get-single-subscription.md) | GET |  |
| [List All Subscriptions](actions/list-all-subscriptions.md) | GET |  |
| [List All Subscriptions By Customer Id](actions/list-all-subscriptions-by-customer-id.md) | GET |  |
| [Subscription Update Charges](actions/subscription-update-charges.md) | PUT |  |
| [Update Subscription](actions/update-subscription.md) | PUT |  |
| [Upgrade Downgrade Subscription](actions/upgrade-downgrade-subscription.md) | PUT |  |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Delete Transaction](actions/delete-transaction.md) | DELETE |  |
| [List All Transactions By Customer Id](actions/list-all-transactions-by-customer-id.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Affiliate Clicks](actions/affiliate-clicks.md) | GET |  |
| [Affiliate Links](actions/affiliate-links.md) | GET |  |
| [Create Commission](actions/create-commission.md) | POST |  |
| [Create Commission Rule](actions/create-commission-rule.md) | POST |  |
| [Create License](actions/create-license.md) | POST |  |
| [Delete Clicks](actions/delete-clicks.md) | DELETE |  |
| [Delete License](actions/delete-license.md) | DELETE |  |
| [Delete License Code](actions/delete-license-code.md) | DELETE |  |
| [Get License Codes](actions/get-license-codes.md) | GET |  |
| [Get Single License](actions/get-single-license.md) | GET |  |
| [List All Licenses](actions/list-all-licenses.md) | GET |  |
| [List Commissions](actions/list-commissions.md) | GET |  |
| [Update Commission](actions/update-commission.md) | PUT |  |
| [Update License](actions/update-license.md) | PUT |  |

