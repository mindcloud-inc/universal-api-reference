# <img src="https://images.mindcloud.co/apps/icons/rye_1775744310148.png" alt="Rye logo" width="28" height="28"> Rye: Universal API

Access Rye's staging Universal Checkout REST API for billing, brands, checkout intents, products, payments, and shipments using a bearer-authenticated API key.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rye/latest
- **Category:** Commerce
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rye.com
- **Vendor API docs:** https://rye.com/docs/api-v2/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Product](actions/lookup-product.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/lookup-product?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Add Payment To Checkout Intent](actions/add-payment-to-checkout-intent.md) | PUT |  |
| [Confirm Checkout Intent](actions/confirm-checkout-intent.md) | PUT | Confirms a checkout intent in Rye. |
| [Create Checkout Intent](actions/create-checkout-intent.md) | POST | Creates a checkout intent in Rye. |
| [Get Checkout Intent](actions/get-checkout-intent.md) | GET | Retrieves a checkout intent from Rye. |
| [List Checkout Intents](actions/list-checkout-intents.md) | GET | Retrieves checkout intents from Rye. |
| [Purchase Product](actions/purchase-product.md) | POST | Creates a product purchase in Rye. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand By Domain](actions/get-brand-by-domain.md) | GET | Finds a brand in Rye by domain. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Top-Up Invoice](actions/create-top-up-invoice.md) | POST | Creates an on-demand top-up invoice in Rye. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Info](actions/get-billing-info.md) | GET | Retrieves billing info from Rye. |
| [Setup Drawdown Billing](actions/setup-drawdown-billing.md) | PUT | Updates drawdown billing settings in Rye. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Get Balance](actions/get-balance.md) | GET | Retrieves the drawdown balance from Rye. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Product](actions/lookup-product.md) | GET | Finds a product in Rye by URL. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Create Checkout Session](actions/create-checkout-session.md) | POST | Creates a checkout session in Rye. |
| [Create Payment Gateway Session](actions/create-payment-gateway-session.md) | POST | Creates a payment gateway session in Rye. |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment](actions/get-shipment.md) | GET | Retrieves a shipment from Rye. |
| [List Checkout Intent Shipments](actions/list-checkout-intent-shipments.md) | GET | Retrieves shipments for a checkout intent in Rye. |
| [List Shipments](actions/list-shipments.md) | GET | Retrieves shipments from Rye. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves drawdown transactions from Rye. |

