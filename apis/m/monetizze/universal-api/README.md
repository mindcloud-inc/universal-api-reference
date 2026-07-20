# <img src="https://images.mindcloud.co/apps/icons/monetizze_1774896899328.png" alt="Monetizze logo" width="28" height="28"> Monetizze: Universal API

Manage Monetizze transactions, subscriptions, checkouts, and billing updates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/monetizze/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.monetizze.com.br
- **Vendor API docs:** https://api.monetizze.com.br/2.1/apidoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Calculate Checkout Installments](actions/calculate-checkout-installments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/calculate-checkout-installments?connectionId=$CONNECTION_ID&ctk=string&reference=string&value=1&maxInstallments=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Generate Access Token](actions/generate-access-token.md) | GET | Retrieves an API access token from Monetizze. |

### Boleto

| Action | Method | Description |
| --- | --- | --- |
| [Update Boleto Due Date](actions/update-boleto-due-date.md) | PUT | Updates a boleto due date in Monetizze. |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Save Ecommerce Checkout](actions/save-ecommerce-checkout.md) | POST | Creates an ecommerce checkout in Monetizze. |

### Checkout Installment

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Checkout Installments](actions/calculate-checkout-installments.md) | GET | Retrieves transparent checkout installment options from Monetizze. |

### Checkout Key

| Action | Method | Description |
| --- | --- | --- |
| [Generate Checkout Key](actions/generate-checkout-key.md) | GET | Retrieves a transparent checkout key from Monetizze. |

### Checkout Order

| Action | Method | Description |
| --- | --- | --- |
| [Process Transparent Checkout Order](actions/process-transparent-checkout-order.md) | POST | Creates a transparent checkout order in Monetizze. |

### Shipment Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Update Sales Tracking](actions/update-sales-tracking.md) | PUT | Updates sales tracking codes in Monetizze. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Update Subscription Plan](actions/update-subscription-plan.md) | PUT | Updates an existing subscription plan in Monetizze. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Search Transactions](actions/search-transactions.md) | GET | Finds transactions in Monetizze by product, email, date, or status. |

