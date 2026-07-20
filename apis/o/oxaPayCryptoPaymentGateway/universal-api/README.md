# <img src="https://images.mindcloud.co/apps/icons/oxa-pay-crypto-payment-gateway_1775854814591.png" alt="OxaPay Crypto Payment Gateway logo" width="28" height="28"> OxaPay Crypto Payment Gateway: Universal API

Accept crypto payments with OxaPay merchant APIs, retrieve payment details, manage static addresses, and read public network and pricing metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oxaPayCryptoPaymentGateway/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oxapay.com
- **Vendor API docs:** https://docs.oxapay.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Payments](actions/list-payments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Accepted Currency List

| Action | Method | Description |
| --- | --- | --- |
| [List Accepted Currencies](actions/list-accepted-currencies.md) | GET | Retrieves accepted currencies from OxaPay. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Generate Invoice](actions/generate-invoice.md) | POST | Creates a new invoice in OxaPay. |
| [Generate White Label](actions/generate-white-label.md) | POST | Creates a new white-label payment in OxaPay. |
| [Get Payment](actions/get-payment.md) | GET | Retrieves a payment from OxaPay. |
| [List Payments](actions/list-payments.md) | GET | Retrieves payments from OxaPay. |

### Price

| Action | Method | Description |
| --- | --- | --- |
| [List Prices](actions/list-prices.md) | GET | Retrieves prices from OxaPay. |

### Static Address

| Action | Method | Description |
| --- | --- | --- |
| [Generate Static Address](actions/generate-static-address.md) | POST | Creates a new static address in OxaPay. |
| [List Static Addresses](actions/list-static-addresses.md) | GET | Retrieves static addresses from OxaPay. |
| [Revoke Static Address](actions/revoke-static-address.md) | DELETE | Deletes an existing static address from OxaPay. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get System Status](actions/get-system-status.md) | GET | Retrieves system status from OxaPay. |

### Supported Currency Map

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Currencies](actions/list-supported-currencies.md) | GET | Retrieves supported currencies from OxaPay. |

### Supported Fiat Currency Map

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Fiat Currencies](actions/list-supported-fiat-currencies.md) | GET | Retrieves supported fiat currencies from OxaPay. |

### Supported Network List

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Networks](actions/list-supported-networks.md) | GET | Retrieves supported networks from OxaPay. |

