# <img src="https://images.mindcloud.co/apps/icons/pinch-payments_1774369511989.png" alt="Pinch Payments logo" width="28" height="28"> Pinch Payments: Universal API

Manage merchants, payers, payments, payment links, refunds, events, and related payment operations in Pinch Payments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pinchPayments/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://getpinch.com.au/
- **Vendor API docs:** https://docs.getpinch.com.au/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Merchant](actions/get-merchant.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-merchant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Checkouts

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Link](actions/create-payment-link.md) | POST | Creates a payment link in Pinch Payments. |
| [Delete Payment Link](actions/delete-payment-link.md) | DELETE | Deletes a payment link from Pinch Payments. |
| [Get Payment Link](actions/get-payment-link.md) | GET | Retrieves a payment link from Pinch Payments. |
| [List Payment Links](actions/list-payment-links.md) | GET | Retrieves payment links from Pinch Payments. |
| [List Payment Links for Payer](actions/list-payment-links-for-payer.md) | GET | Retrieves payment links for a payer from Pinch Payments. |

### Company Infos

| Action | Method | Description |
| --- | --- | --- |
| [Get Merchant](actions/get-merchant.md) | GET | Retrieves your merchant details from Pinch Payments. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Payer](actions/create-or-update-payer.md) | POST | Creates or updates a payer in Pinch Payments. |
| [Delete Payer](actions/delete-payer.md) | DELETE | Deletes an existing payer from Pinch Payments. |
| [Get Payer](actions/get-payer.md) | GET | Retrieves a payer from Pinch Payments. |
| [List Payers](actions/list-payers.md) | GET | Retrieves payers from Pinch Payments. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Get Event](actions/get-event.md) | GET | Retrieves an event from Pinch Payments. |
| [List Events](actions/list-events.md) | GET | Retrieves events from Pinch Payments. |

### Payment Methods

| Action | Method | Description |
| --- | --- | --- |
| [Create Payment Source](actions/create-payment-source.md) | POST | Creates a payment source in Pinch Payments. |
| [Delete Payment Source](actions/delete-payment-source.md) | DELETE | Deletes a payment source from Pinch Payments. |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Payment](actions/create-or-update-payment.md) | POST | Creates or updates a scheduled payment in Pinch Payments. |
| [Create Realtime Payment](actions/create-realtime-payment.md) | POST | Creates a realtime payment in Pinch Payments. |
| [Delete Payment](actions/delete-payment.md) | DELETE | Deletes an existing payment from Pinch Payments. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from Pinch Payments. |
| [List Payments for Payer](actions/list-payments-for-payer.md) | GET | Retrieves payments for a payer from Pinch Payments. |
| [List Processed Payments](actions/list-processed-payments.md) | GET | Retrieves processed payments from Pinch Payments. |
| [List Scheduled Payments](actions/list-scheduled-payments.md) | GET | Retrieves scheduled payments from Pinch Payments. |

### Refunds

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund in Pinch Payments. |
| [Get Refund](actions/get-refund.md) | GET | Retrieves a refund from Pinch Payments. |
| [List Refunds](actions/list-refunds.md) | GET | Retrieves refunds from Pinch Payments. |

