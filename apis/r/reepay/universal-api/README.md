# <img src="https://images.mindcloud.co/apps/icons/id-wvap25br-logos_1775071518315.jpeg" alt="Reepay logo" width="28" height="28"> Reepay: Universal API

Manage subscriptions, customers, invoices, and payment methods

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reepay/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://frisbii.com
- **Vendor API docs:** https://docs.frisbii.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reepay/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Agreement

| Action | Method | Description |
| --- | --- | --- |
| [Create Offline Agreement](actions/create-offline-agreement.md) | POST | Creates an offline agreement in Reepay. |
| [Delete Gateway Agreement](actions/delete-gateway-agreement.md) | DELETE | Deletes a gateway agreement from Reepay. |
| [Get Gateway Agreement](actions/get-gateway-agreement.md) | GET | Retrieves a gateway agreement from Reepay. |

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Charge](actions/cancel-charge.md) | PUT | Cancels a charge in Reepay. |
| [Cancel Invoice Transaction](actions/cancel-invoice-transaction.md) | PUT | Cancels an invoice transaction in Reepay. |
| [Create Charge](actions/create-charge.md) | POST | Creates a new charge in Reepay. |
| [Get Charge](actions/get-charge.md) | GET | Retrieves a charge from Reepay. |
| [List Charges](actions/list-charges.md) | GET | Retrieves charges from Reepay. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in Reepay. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from Reepay. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from Reepay. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Reepay. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in Reepay. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Invoice](actions/cancel-invoice.md) | PUT | Cancels an invoice in Reepay. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Reepay. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Reepay. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Add Offline Payment Method](actions/add-offline-payment-method.md) | POST | Adds an offline payment method in Reepay. |
| [Add Payment Method](actions/add-payment-method.md) | POST | Adds a payment method in Reepay. |
| [Delete Payment Method](actions/delete-payment-method.md) | DELETE | Deletes a payment method from Reepay. |
| [Get Payment Method](actions/get-payment-method.md) | GET | Retrieves a payment method from Reepay. |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Reepay. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a new plan in Reepay. |
| [Delete Plan](actions/delete-plan.md) | DELETE | Deletes an existing plan from Reepay. |
| [Get Current Plan](actions/get-current-plan.md) | GET | Retrieves the current plan from Reepay. |
| [List Plans](actions/list-plans.md) | GET | Retrieves plans from Reepay. |
| [Update Plan](actions/update-plan.md) | PUT | Updates an existing plan in Reepay. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | PUT | Cancels a subscription in Reepay. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in Reepay. |
| [Delete Pending Subscription](actions/delete-pending-subscription.md) | DELETE | Deletes a pending subscription from Reepay. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from Reepay. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from Reepay. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in Reepay. |

