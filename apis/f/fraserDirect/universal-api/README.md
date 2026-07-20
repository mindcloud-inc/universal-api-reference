# <img src="https://mindcloud.imgix.net/apps/icons/download_1781285392080.jpeg" alt="Fraser Direct logo" width="28" height="28"> Fraser Direct: Universal API

Fraser Direct warehouse management and fulfillment API for orders, shipment lookups, inventory, purchase orders, and inventory adjustments.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fraserDirect/latest
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fraserdirect.ca/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get inventory](actions/get-inventory.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory?connectionId=$CONNECTION_ID&groupByLot=N&includeInPick=N" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Inventory Items

| Action | Method | Description |
| --- | --- | --- |
| [Get inventory](actions/get-inventory.md) | GET |  |
| [Get inventory adjustments](actions/get-inventory-adjustments.md) | GET |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create order](actions/create-order.md) | POST |  |
| [Create purchase order](actions/create-purchase-order.md) | POST |  |
| [Get order information](actions/get-order-information.md) | GET |  |

### Shipments

| Action | Method | Description |
| --- | --- | --- |
| [Get order shipping information](actions/get-order-shipping-information.md) | GET |  |
| [Get purchase order information](actions/get-purchase-order-information.md) | GET |  |

