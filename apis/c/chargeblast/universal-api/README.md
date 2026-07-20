# <img src="https://images.mindcloud.co/apps/icons/favicon_1776441529529.png" alt="Chargeblast logo" width="28" height="28"> Chargeblast: Universal API

Chargeblast helps merchants prevent chargebacks through alerts, digital receipts, deflections, merchant enrollment, and related API-driven dispute-prevention workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/chargeblast/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.chargeblast.com/
- **Vendor API docs:** https://docs.chargeblast.com/api-reference/getting-started/guide

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Alerts](actions/fetch-alerts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Alerts](actions/fetch-alerts.md) | GET | Retrieves alerts from Chargeblast. |

### Deflection Log

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Deflection Logs](actions/fetch-deflection-logs.md) | GET | Retrieves deflection logs from Chargeblast. |

### Descriptor

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Descriptors](actions/fetch-descriptors.md) | GET | Retrieves descriptors from Chargeblast. |

### Ip Data

| Action | Method | Description |
| --- | --- | --- |
| [Upload IP Data](actions/upload-ip-data.md) | POST | Uploads IP data to Chargeblast. |

### Merchant

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Merchant](actions/fetch-merchant.md) | GET | Retrieves a merchant from Chargeblast. |
| [Fetch Merchants](actions/fetch-merchants.md) | GET | Retrieves merchants from Chargeblast. |

### Order

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Order](actions/fetch-order.md) | GET | Retrieves an order from Chargeblast. |
| [Fetch Orders](actions/fetch-orders.md) | GET | Retrieves orders from Chargeblast. |
| [Upload Orders](actions/upload-orders.md) | POST | Uploads orders to Chargeblast. |

