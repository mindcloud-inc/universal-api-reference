# Get Purchase Order with inFlow Inventory

Retrieves an existing purchase order from inFlow Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/purchase-orders/:purchaseOrderId`
- **Base URL:** `https://cloudapi.inflowinventory.com/{companyId}`
- **Official documentation:** [Get Purchase Order](https://cloudapi.inflowinventory.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchaseOrderId` | path | `string` | yes | The unique identifier of the purchase order to retrieve. |
