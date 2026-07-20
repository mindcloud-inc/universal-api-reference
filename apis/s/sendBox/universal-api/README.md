# <img src="https://images.mindcloud.co/apps/icons/sendbox-icon-square_1776455533473.png" alt="SendBox logo" width="28" height="28"> SendBox: Universal API

SendBox shipping and payments API for shipment quotes, shipment creation, tracking, saved addresses, payment profile, and virtual account access.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sendBox/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sendbox.co
- **Vendor API docs:** https://docs.sendbox.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Saved Addresses](actions/list-saved-addresses.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendBox/latest/actions/list-saved-addresses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Addresses](actions/list-saved-addresses.md) | GET |  |

### Landed Cost Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Landed Cost](actions/calculate-landed-cost.md) | GET |  |

### Payment Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Payment Profile](actions/get-payment-profile.md) | GET |  |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST |  |
| [Get Shipment](actions/get-shipment.md) | GET |  |
| [List Shipments](actions/list-shipments.md) | GET |  |

### Shipment Tracking

| Action | Method | Description |
| --- | --- | --- |
| [Track Shipment](actions/track-shipment.md) | GET |  |

### Shipping Quote

| Action | Method | Description |
| --- | --- | --- |
| [Request Shipping Quotes](actions/request-shipping-quotes.md) | GET |  |

### Virtual Account

| Action | Method | Description |
| --- | --- | --- |
| [List Virtual Accounts](actions/list-virtual-accounts.md) | GET |  |

