# <img src="https://images.mindcloud.co/apps/icons/cheddar_1774877178473.png" alt="Cheddar logo" width="28" height="28"> Cheddar: Universal API

Cheddar handles subscription billing with pricing plans, customer subscriptions, tracked usage, invoices, charges, refunds, and promotions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cheddar/latest
- **Category:** Commerce
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getcheddar.com
- **Vendor API docs:** https://docs.getcheddar.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pricing Plans](actions/list-pricing-plans.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Add Custom Charge or Credit](actions/add-custom-charge-or-credit.md) | POST | Creates a custom charge or credit in Cheddar. |
| [Delete Custom Charge or Credit](actions/delete-custom-charge-or-credit.md) | DELETE | Deletes a custom charge or credit from Cheddar. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer and subscription in Cheddar. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Cheddar. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves customer billing details from Cheddar. |
| [Import Customers](actions/import-customers.md) | POST | Imports existing customer records into Cheddar. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customer billing records from Cheddar. |
| [Update Customer](actions/update-customer.md) | PUT | Updates existing customer details in Cheddar. |
| [Update Customer and Subscription](actions/update-customer-and-subscription.md) | PUT | Updates customer and subscription details in Cheddar. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create One-Time Invoice](actions/create-one-time-invoice.md) | POST | Creates a one-time invoice in Cheddar. |
| [Issue Void](actions/issue-void.md) | PUT | Voids a billed invoice transaction in Cheddar. |
| [Issue Void or Refund](actions/issue-void-or-refund.md) | PUT | Voids or refunds a billed invoice in Cheddar. |
| [Run Outstanding Invoice](actions/run-outstanding-invoice.md) | PUT | Executes an outstanding invoice in Cheddar. |
| [Send or Resend Invoice Email](actions/send-or-resend-invoice-email.md) | PUT | Sends or resends an invoice email in Cheddar. |

### Pricing Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get Pricing Plan](actions/get-pricing-plan.md) | GET | Retrieves pricing plan details from Cheddar. |
| [List Pricing Plans](actions/list-pricing-plans.md) | GET | Retrieves pricing plan records from Cheddar. |

### Promotion

| Action | Method | Description |
| --- | --- | --- |
| [Get Promotion](actions/get-promotion.md) | GET | Retrieves promotion coupon details from Cheddar. |
| [List Promotions](actions/list-promotions.md) | GET | Retrieves promotion coupon records from Cheddar. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Issue Refund](actions/issue-refund.md) | POST | Creates a refund for a billed invoice in Cheddar. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels an existing customer subscription in Cheddar. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Cheddar. |

### Tracked Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Item Quantity](actions/add-item-quantity.md) | PUT | Increments a customer item quantity in Cheddar. |
| [Remove Item Quantity](actions/remove-item-quantity.md) | PUT | Decrements a customer item quantity in Cheddar. |
| [Set Item Quantity](actions/set-item-quantity.md) | PUT | Sets a customer item quantity in Cheddar. |

