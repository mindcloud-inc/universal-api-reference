# <img src="https://images.mindcloud.co/apps/icons/charge-desk_1776102033114.png" alt="ChargeDesk logo" width="28" height="28"> ChargeDesk: Universal API

ChargeDesk helps support teams manage billing data, charges, customers, subscriptions, products, webhooks, and billing activity across connected payment gateways.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargeDesk/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://chargedesk.com
- **Vendor API docs:** https://chargedesk.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Charges](actions/list-charges.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeDesk/latest/actions/list-charges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Agent Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Agent Activity](actions/list-agent-activity.md) | GET | Retrieves agent activity logs from ChargeDesk. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Create Charge](actions/create-charge.md) | POST | Creates a new charge in ChargeDesk. |
| [List Charges](actions/list-charges.md) | GET | Retrieves charges from ChargeDesk. |
| [Retrieve Charge](actions/retrieve-charge.md) | GET | Retrieves a charge from ChargeDesk. |
| [Update Charge](actions/update-charge.md) | PUT | Updates an existing charge in ChargeDesk. |

### Charge Email

| Action | Method | Description |
| --- | --- | --- |
| [Email Charge](actions/email-charge.md) | POST | Emails a charge from ChargeDesk. |

### Charge Item

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Charge Items](actions/retrieve-charge-items.md) | GET | Retrieves charge items from ChargeDesk. |

### Charge Preview

| Action | Method | Description |
| --- | --- | --- |
| [Preview Charge](actions/preview-charge.md) | GET | Retrieves a charge preview from ChargeDesk. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in ChargeDesk. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from ChargeDesk. |
| [Retrieve Customer](actions/retrieve-customer.md) | GET | Retrieves a customer from ChargeDesk. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in ChargeDesk. |

### Customer Group

| Action | Method | Description |
| --- | --- | --- |
| [Group Customers](actions/group-customers.md) | GET | Retrieves grouped customers from ChargeDesk. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST | Creates a new product in ChargeDesk. |
| [List Products](actions/list-products.md) | GET | Retrieves products from ChargeDesk. |
| [Retrieve Product](actions/retrieve-product.md) | GET | Retrieves a product from ChargeDesk. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in ChargeDesk. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Create Subscription](actions/create-subscription.md) | POST | Creates a new subscription in ChargeDesk. |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves subscriptions from ChargeDesk. |
| [Retrieve Subscription](actions/retrieve-subscription.md) | GET | Retrieves a subscription from ChargeDesk. |
| [Update Subscription](actions/update-subscription.md) | PUT | Updates an existing subscription in ChargeDesk. |

### Subscription Cancellation

| Action | Method | Description |
| --- | --- | --- |
| [List Subscription Cancellations](actions/list-subscription-cancellations.md) | GET | Retrieves subscription cancellations from ChargeDesk. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in ChargeDesk. |

### Webhook Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Webhook Notifications](actions/list-webhook-notifications.md) | GET | Retrieves webhook notifications from ChargeDesk. |

