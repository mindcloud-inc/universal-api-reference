# Update Inventory with Walmart

Replace the stock level for one SKU.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/inventory`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Update Inventory](https://developer.walmart.com/us-marketplace/reference/updateinventoryforanitem)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `quantity.unit` | body | `string` | no | A unit of measure. Walmart Marketplace supports only EACH which indicates one individual sellable item. |
| `sku` | query | `string` | yes | A unique alphanumeric ID you assign to each item. Use the same value in every request that references the item, including your XSD catalog file. Format: `toggle`. |
| `sku` | body | `string` | yes | — |
| `quantity` | body | `object` | no | The quantity that customers have ordered but you haven't shipped yet. |
| `quantity.amount` | body | `number` | no | The number of units pending shipment. |
| `inventoryAvailableDate` | body | `string` | no | The date when this inventory becomes available at the ship node. Use ISO 8601 format (YYYY-MM-DD). If you omit this field, Walmart treats the inventory as available today. |
| `shipNode` | query | `list<string>` | no | The unique ID of the ship node (fulfillment center) where you want to update inventory. If you omit this parameter, Walmart updates inventory at your default ship node. |
| `isDynamicSandbox` | query | `boolean` | no | — |
