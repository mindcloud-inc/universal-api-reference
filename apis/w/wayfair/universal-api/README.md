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

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Get Bill of Lading](actions/get-bill-of-lading.md) | GET |  |

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [Update Item List Inventory](actions/update-inventory-list.md) | PUT |  |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Get Packing Slip](actions/get-packing-slip.md) | GET |  |
| [Get Shipping Label](actions/get-shipping-label.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Accept Order](actions/accept-order.md) | PUT |  |
| [Acknowledge Castle Gate Order](actions/acknowledge-castle-gate-order.md) | PUT |  |
| [Get CastleGate Orders](actions/get-castle-gate-orders.md) | GET |  |
| [Get Dropship Orders](actions/get-dropship-orders.md) | GET |  |
| [Register Order](actions/register-order.md) | PUT | Register purchase order items for shipment |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [GraphQL](actions/graph-ql.md) | POST |  |
| [test](actions/test.md) | GET |  |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge CastleGate Shipping Advice](actions/acknowledge-castle-gate-shipping-advice.md) | PUT |  |
| [Get CastleGate Orders Shipping Advice](actions/get-castle-gate-shipping-advice.md) | GET |  |
| [Send Shipment Notice](actions/send-shipment-notice.md) | PUT |  |

