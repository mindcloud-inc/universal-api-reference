# Get Stock Adjustment with inFlow Inventory

Retrieves an existing stock adjustment from inFlow Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock-adjustments/:stockAdjustmentId`
- **Base URL:** `https://cloudapi.inflowinventory.com/{companyId}`
- **Official documentation:** [Get Stock Adjustment](https://cloudapi.inflowinventory.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stockAdjustmentId` | path | `string` | yes | The unique identifier of the stock adjustment to retrieve. |
