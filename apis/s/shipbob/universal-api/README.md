# <img src="https://images.mindcloud.co/apps/icons/shipbob-icon_1782394422728.svg" alt="ShipBob logo" width="28" height="28"> ShipBob: Universal API

ShipBob through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shipbob/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Inventory Levels by Location](actions/list-inventory-levels-by-location.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipbob/latest/actions/list-inventory-levels-by-location?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Inventories

| Action | Method | Description |
| --- | --- | --- |
| [Get Inventory Level](actions/get-inventory-level.md) | GET |  |
| [List Inventory Levels by Location](actions/list-inventory-levels-by-location.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Fulfillment Centers](actions/get-fulfillment-centers.md) | GET |  |
| [Get Multiple Products](actions/get-multiple-products.md) | GET |  |
| [Get Multiple Warehouse Receiving Orders](actions/get-multiple-warehouse-receiving-orders.md) | GET |  |
| [Get Warehouse Receiving Order](actions/get-warehouse-receiving-order.md) | GET |  |
| [Get Warehouse Receivng Order Boxes](actions/get-warehouse-receivng-order-boxes.md) | GET |  |
| [List Inventory Items](actions/list-inventory-items.md) | GET |  |
| [Post Product](actions/post-product.md) | POST |  |
| [Post Warehouse Receiving Order](actions/post-warehouse-receiving-order.md) | POST |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |

### Return Order

| Action | Method | Description |
| --- | --- | --- |
| [Get Return Order](actions/get-return-order.md) | GET |  |
| [List Return Orders](actions/list-return-orders.md) | GET |  |

### Sales Orders

| Action | Method | Description |
| --- | --- | --- |
| [Get Orders](actions/get-orders.md) | GET |  |

