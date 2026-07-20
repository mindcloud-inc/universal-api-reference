# <img src="https://images.mindcloud.co/apps/icons/mercado-pago-notifications_1774555846692.png" alt="Mercado Pago logo" width="28" height="28"> Mercado Pago: Universal API

Production-ready Mercado Pago wrapper centered on notification-topic readbacks and the checkout/payment resources that emit those notifications.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mercadoPago/latest
- **Category:** Commerce
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mercadopago.com/
- **Vendor API docs:** https://www.mercadopago.com.ar/developers/en/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payment Methods](actions/list-payment-methods.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/list-payment-methods?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Chargeback](actions/get-chargeback.md) | GET | Retrieves a chargeback from Mercado Pago. |

### Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Create Preference](actions/create-preference.md) | POST | Creates a checkout preference in Mercado Pago. |
| [Get Preference](actions/get-preference.md) | GET | Retrieves a checkout preference from Mercado Pago. |
| [Search Preferences](actions/search-preferences.md) | GET | Finds checkout preferences in Mercado Pago by filter criteria. |
| [Update Preference](actions/update-preference.md) | PUT | Updates an existing checkout preference in Mercado Pago. |

### Claim

| Action | Method | Description |
| --- | --- | --- |
| [Get Claim Details](actions/get-claim-details.md) | GET | Retrieves claim details from Mercado Pago. |
| [Search Claims](actions/search-claims.md) | GET | Finds claims in Mercado Pago by filter criteria. |

### Claim Evidence

| Action | Method | Description |
| --- | --- | --- |
| [Get Claim Evidence](actions/get-claim-evidence.md) | GET | Retrieves claim evidence from Mercado Pago. |

### Claim History

| Action | Method | Description |
| --- | --- | --- |
| [Get Claim History](actions/get-claim-history.md) | GET | Retrieves claim status history from Mercado Pago. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice Data](actions/get-invoice-data.md) | GET | Retrieves invoice data from Mercado Pago. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Order](actions/get-order.md) | GET | Retrieves an order from Mercado Pago. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Cancellation](actions/create-cancellation.md) | PUT | Cancels a payment in Mercado Pago. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from Mercado Pago. |
| [Search Payments](actions/search-payments.md) | GET | Finds payments in Mercado Pago by filter criteria. |

### Payment Method

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Methods](actions/list-payment-methods.md) | GET | Retrieves payment methods from Mercado Pago. |

### Purchase Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant Order](actions/get-merchant-order.md) | GET | Retrieves a merchant order from Mercado Pago. |
| [Search Merchant Orders](actions/search-merchant-orders.md) | GET | Finds merchant orders in Mercado Pago by filter criteria. |
| [Update Merchant Order](actions/update-merchant-order.md) | PUT | Updates an existing merchant order in Mercado Pago. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund in Mercado Pago. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves a refund from Mercado Pago. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves refunds for a payment from Mercado Pago. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Search Subscriptions](actions/search-subscriptions.md) | GET | Finds subscriptions in Mercado Pago by filter criteria. |

### Subscription Plan

| Action | Method | Description |
| --- | --- | --- |
| [Search Subscription Plans](actions/search-subscription-plans.md) | GET | Finds subscription plans in Mercado Pago by filter criteria. |

