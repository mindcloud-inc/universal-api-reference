# <img src="https://images.mindcloud.co/apps/icons/wayfair-icon_1782394711224.jpg" alt="Wayfair logo" width="28" height="28"> Wayfair: Universal API

Wayfair through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wayfair/latest
- **Category:** Commerce
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://developer.wayfair.io/posts/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bill of Lading](actions/get-bill-of-lading.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-bill-of-lading?connectionId=$CONNECTION_ID&purchaseOrderNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Accept Order](actions/accept-order.md) | POST |  |
| [Acknowledge Castle Gate Order](actions/acknowledge-castle-gate-order.md) | POST |  |
| [Acknowledge CastleGate Shipping Advice](actions/acknowledge-castle-gate-shipping-advice.md) | POST |  |
| [Get Bill of Lading](actions/get-bill-of-lading.md) | GET |  |
| [Get CastleGate Orders](actions/get-castle-gate-orders.md) | GET |  |
| [Get CastleGate Orders Shipping Advice](actions/get-castle-gate-shipping-advice.md) | POST |  |
| [Get Dropship Orders](actions/get-dropship-orders.md) | POST |  |
| [Get Packing Slip](actions/get-packing-slip.md) | GET |  |
| [Get Shipping Label](actions/get-shipping-label.md) | GET |  |
| [GraphQL](actions/graph-ql.md) | POST |  |
| [Register Order](actions/register-order.md) | POST | Register purchase order items for shipment |
| [Send Shipment Notice](actions/send-shipment-notice.md) | POST |  |
| [test](actions/test.md) | GET |  |
| [Update Item List Inventory](actions/update-inventory-list.md) | POST |  |

