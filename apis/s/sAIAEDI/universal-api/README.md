# <img src="https://images.mindcloud.co/apps/icons/saia-icon_1777653375601.png" alt="SAIA EDI logo" width="28" height="28"> SAIA EDI: Universal API

Saia LTL Freight XML API integration for shipment lookup, pickup scheduling, and bill-of-lading workflows using Saia Developer Portal API-key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sAIAEDI/latest
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.saia.com
- **Vendor API docs:** https://saiaprodapi.developer.azure-api.net/api-details

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Shipment by PRO Number](actions/get-shipment-by-pro-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAIAEDI/latest/actions/get-shipment-by-pro-number?connectionId=$CONNECTION_ID&ProNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Bill Of Lading

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill of Lading](actions/create-bill-of-lading.md) | POST | Creates a bill of lading in SAIA EDI. |

### Pickup

| Action | Method | Description |
| --- | --- | --- |
| [Create Pickup Request](actions/create-pickup-request.md) | POST | Creates a pickup request in SAIA EDI. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Shipment by Bill of Lading Number](actions/get-shipment-by-bill-of-lading-number.md) | GET | Retrieves a shipment from SAIA EDI by bill of lading number. |
| [Get Shipment by PO Number](actions/get-shipment-by-po-number.md) | GET | Retrieves a shipment from SAIA EDI by PO number. |
| [Get Shipment by PRO Number](actions/get-shipment-by-pro-number.md) | GET | Retrieves a shipment from SAIA EDI by PRO number. |

