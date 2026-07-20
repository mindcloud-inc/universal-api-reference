# <img src="https://images.mindcloud.co/apps/icons/billwerkplus_1776199731926.png" alt="Billwerkplus logo" width="28" height="28"> Billwerkplus: Universal API

Manage billing, subscriptions, payments, and customer accounts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/billwerkplus/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frisbii.com/
- **Vendor API docs:** https://docs.frisbii.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-current-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/get-current-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-current-account.md) | GET | Retrieves current account details from Billwerkplus. |

### Add-on

| Action | Method | Description |
| --- | --- | --- |
| [Create Add-On](actions/create-addon.md) | POST | Creates an add-on in Billwerkplus. |
| [Get Add-On](actions/get-add-on.md) | GET | Retrieves an add-on from Billwerkplus. |
| [List Add-Ons](actions/list-add-ons.md) | GET | Retrieves add-ons from Billwerkplus. |
| [Update Add-On](actions/update-addon.md) | PUT | Updates an add-on in Billwerkplus. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Charge](actions/get-charge.md) | GET | Retrieves a charge from Billwerkplus. |
| [List Charges](actions/list-charges.md) | GET | Retrieves charges from Billwerkplus. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in Billwerkplus. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Soft-deletes a customer from Billwerkplus. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Billwerkplus. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Billwerkplus. |
| [Update Customer](actions/update-customer.md) | PUT | Updates a customer in Billwerkplus. |

### Dispute

| Action | Method | Description |
| --- | --- | --- |
| [List Disputes](actions/list-disputes.md) | GET | Retrieves disputes from Billwerkplus. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | PUT | Cancels an invoice in Billwerkplus. |
| [Create Invoice for Customer](actions/create-invoice-for-customer.md) | POST | Creates an invoice for a Billwerkplus customer. |
| [Create On-Demand Subscription Invoice](actions/create-on-demand-subscription-invoice.md) | POST | Creates an on-demand invoice for a Billwerkplus subscription. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Billwerkplus. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Billwerkplus. |
| [Reactivate Invoice](actions/reactivate-invoice.md) | PUT | Reactivates an invoice in Billwerkplus. |

### Invoice Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Next Subscription Invoice](actions/preview-next-subscription-invoice.md) | GET | Retrieves the next invoice preview for a Billwerkplus subscription. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [Get Subscription Payment Method](actions/get-subscription-payment-method.md) | GET | Retrieves the payment method for a Billwerkplus subscription. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Billwerkplus. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a plan in Billwerkplus. |
| [Get Plan](actions/get-plan.md) | GET | Retrieves a plan from Billwerkplus. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from Billwerkplus. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE | Cancels a subscription in Billwerkplus. |
| [Change Next Renewal Date](actions/change-next-renewal-date.md) | PUT | Updates a subscription's next renewal date in Billwerkplus. |
| [Change Subscription](actions/change-subscription.md) | PUT | Updates a subscription plan or quantity in Billwerkplus. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a subscription in Billwerkplus. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Billwerkplus. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Billwerkplus. |
| [Put Subscription On Hold](actions/put-subscription-on-hold.md) | PUT | Puts a subscription on hold in Billwerkplus. |
| [Reactivate Subscription](actions/reactivate-subscription.md) | PUT | Reactivates a subscription on hold in Billwerkplus. |

