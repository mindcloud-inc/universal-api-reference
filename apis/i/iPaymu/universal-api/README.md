# <img src="https://images.mindcloud.co/apps/icons/id-m3sl-fd-s-logos_1776885620060.png" alt="iPaymu logo" width="28" height="28"> iPaymu: Universal API

Accept payments and manage balances and payment transactions

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iPaymu/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ipaymu.com
- **Vendor API docs:** https://ipaymu.com/api-collection/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Balance](actions/check-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Check your iPaymu account balance. |

### Coverage Area

| Action | Method | Description |
| --- | --- | --- |
| [Get COD Coverage Area](actions/get-cod-coverage-area.md) | GET | Check whether a location is covered by iPaymu cash-on-delivery service. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Payment](actions/create-direct-payment.md) | POST | Create a direct payment and return the payment details for the selected channel. |
| [Create Redirect Payment](actions/create-redirect-payment.md) | POST | Create a payment session that redirects the buyer to the iPaymu payment page. |

### Payment Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Payment Channels](actions/list-payment-channels.md) | GET | List available iPaymu payment channels. |

### Pickup Request

| Action | Method | Description |
| --- | --- | --- |
| [Request COD Pickup](actions/request-cod-pickup.md) | POST | Create an iPaymu cash-on-delivery pickup request. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Track COD Shipment](actions/track-cod-shipment.md) | GET | Track the status of an iPaymu cash-on-delivery shipment. |

### Shipping Label

| Action | Method | Description |
| --- | --- | --- |
| [Download COD Label](actions/download-cod-label.md) | GET | Download the shipping label for an iPaymu cash-on-delivery transaction. |

### Shipping Quote

| Action | Method | Description |
| --- | --- | --- |
| [Calculate COD Shipping](actions/calculate-cod-shipping.md) | GET | Calculate shipping costs for an iPaymu cash-on-delivery shipment. |

### Transaction

| Action | Method | Description |
| --- | --- | --- |
| [Check Transaction](actions/check-transaction.md) | GET | Get realtime details and status for an iPaymu transaction. |
| [List Transaction History](actions/list-transaction-history.md) | GET | List your iPaymu transaction history. |

