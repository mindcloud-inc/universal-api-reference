# Get Single Item Inventory by Ship Node with Walmart

Retrieve the current stock for one SKU at one or multiple ship nodes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/inventories/:sku`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Single Item Inventory by Ship Node](https://developer.walmart.com/us-marketplace/reference/getmultinodeinventoryforskuandallshipnodes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipNode` | query | `list<list>` | no | The unique ID of the ship node (fulfillment center) whose inventory you want to retrieve. If you omit this parameter, the response includes inventory for every ship node linked to your seller account |
| `sku` | path | `string` | yes | A unique alphanumeric ID you assign to each item. Use the same value in every request that references the item, including your XSD catalog file. Format: `toggle`. |
