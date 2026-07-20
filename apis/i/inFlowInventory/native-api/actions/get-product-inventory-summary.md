# Get Product Inventory Summary with inFlow Inventory

Retrieves a product inventory summary from inFlow Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/products/:productId/summary`
- **Base URL:** `https://cloudapi.inflowinventory.com/{companyId}`
- **Official documentation:** [Get Product Inventory Summary](https://cloudapi.inflowinventory.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `productId` | path | `string` | yes | The inFlow product ID. |
