# <img src="https://images.mindcloud.co/apps/icons/pay-whirl_1775576504140.png" alt="PayWhirl logo" width="28" height="28"> PayWhirl: Universal API

Manage PayWhirl customers, plans, subscriptions, invoices, charges, and saved cards through the official PayWhirl API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/payWhirl/latest
- **Category:** Commerce
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.paywhirl.com
- **Vendor API docs:** https://api.paywhirl.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Test Connection](actions/test-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Address](actions/create-customer-address.md) | POST | Creates a new customer address in PayWhirl. |
| [Delete Customer Address](actions/delete-customer-address.md) | DELETE | Deletes an existing customer address from PayWhirl. |
| [Get Customer Address](actions/get-customer-address.md) | GET | Retrieves a customer address from PayWhirl by ID. |
| [List Customer Addresses](actions/list-customer-addresses.md) | GET | Retrieves a customer's addresses from PayWhirl. |
| [Update Customer Address](actions/update-customer-address.md) | PUT | Updates an existing customer address in PayWhirl. |

### Charges

| Action | Method | Description |
| --- | --- | --- |
| [Create Charge](actions/create-charge.md) | POST | Creates a new charge in PayWhirl. |
| [Get Charge](actions/get-charge.md) | GET | Retrieves a charge from PayWhirl by ID. |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Test Connection](actions/test-connection.md) | GET | Retrieves connection details from PayWhirl. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in PayWhirl. |
| [Delete Customer](actions/delete-customer.md) | DELETE | Deletes an existing customer from PayWhirl. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from PayWhirl by ID. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from PayWhirl. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in PayWhirl. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Add Promo To Invoice](actions/add-promo-to-invoice.md) | PUT | Adds a promo code to a PayWhirl invoice. |
| [Change Invoice Payment Method](actions/change-invoice-payment-method.md) | PUT | Changes an invoice's payment method in PayWhirl. |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in PayWhirl. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from PayWhirl. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from PayWhirl by ID. |
| [List Customer Invoices](actions/list-customer-invoices.md) | GET | Retrieves a customer's invoices from PayWhirl. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from PayWhirl. |
| [Mark Invoice As Paid](actions/mark-invoice-as-paid.md) | PUT | Marks an invoice as paid in PayWhirl. |
| [Process Invoice](actions/process-invoice.md) | PUT | Processes an invoice in PayWhirl. |
| [Remove Promo From Invoice](actions/remove-promo-from-invoice.md) | PUT | Removes a promo code from a PayWhirl invoice. |
| [Update Invoice Items](actions/update-invoice-items.md) | PUT | Updates invoice line items in PayWhirl. |
| [Update Invoice Next Payment Date](actions/update-invoice-next-payment-date.md) | PUT | Updates an invoice's next payment date in PayWhirl. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | POST | Creates a new card in PayWhirl. |
| [Delete Card](actions/delete-card.md) | DELETE | Deletes an existing card from PayWhirl. |
| [Get Card](actions/get-card.md) | GET | Retrieves a card from PayWhirl by ID. |
| [List Customer Cards](actions/list-customer-cards.md) | GET | Retrieves a customer's cards from PayWhirl. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund for a PayWhirl charge. |

### Subscribers

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribers](actions/list-subscribers.md) | GET | Retrieves subscribers from PayWhirl. |

### Subscription Plans

| Action | Method | Description |
| --- | --- | --- |
| [Create Plan](actions/create-plan.md) | POST | Creates a new subscription plan in PayWhirl. |
| [Get Plan](actions/get-plan.md) | GET | Retrieves a subscription plan from PayWhirl by ID. |
| [List Plans](actions/list-plans.md) | GET | Retrieves subscription plans from PayWhirl. |
| [Update Plan](actions/update-plan.md) | PUT | Updates an existing subscription plan in PayWhirl. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Subscription](actions/cancel-subscription.md) | DELETE | Cancels a subscription in PayWhirl. |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in PayWhirl. |
| [Get Subscription](actions/get-subscription.md) | GET | Retrieves a subscription from PayWhirl by ID. |
| [List Customer Subscriptions](actions/list-customer-subscriptions.md) | GET | Retrieves a customer's subscriptions from PayWhirl. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in PayWhirl. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Profile](actions/get-customer-profile.md) | GET | Retrieves a customer's profile from PayWhirl. |

