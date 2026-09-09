# Bulk Item Inventory Update with Walmart

Upload a feed file to update inventory for multiple SKUs.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/feeds`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Bulk Item Inventory Update](https://developer.walmart.com/us-marketplace/reference/post_v3-feeds)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedType` | query | `list` | yes | -`inventory` - Single ship node per file (spec 1.4). JSON or XML. -`MP_INVENTORY` - Multiple ship nodes per SKU (spec 1.5). JSON only. |
| `Inventory[].quantity.unit` | body | `string` | no | EACH |
| `Inventory[].sku` | body | `string` | no | — |
| `InventoryHeader` | body | `object` | no | — |
| `InventoryHeader.version` | body | `string` | no | — |
| `Inventory[].quantity` | body | `object` | no | — |
| `Inventory[].quantity.amount` | body | `number` | no | — |
| `Inventory[]` | body | `array<object>` | no | — |
| `Inventory[].inventoryAvailableDate` | body | `string` | no | YYYY-MM-DD |
