# Get Inventory with Walmart

Retrieve the current inventory for a single SKU.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/inventory`
- **Base URL:** `https://{environment}.walmartapis.com`
- **API:** REST
- **Official documentation:** [Get Inventory](https://developer.walmart.com/us-marketplace/reference/getallitems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shipNode` | query | `list<list>` | no | The unique ID of the ship node (fulfillment center) whose inventory you want to retrieve. If you omit this parameter, the response includes inventory for every ship node linked to your seller account. |
| `sku` | query | `string` | yes | A unique alphanumeric ID you assign to each item. Use the same value in every request that references the item, including your XSD catalog file. Format: `toggle`. |
| `isDynamicSandbox` | query | `boolean` | no | — |
