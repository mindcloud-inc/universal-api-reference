# Get Stock Transfer with inFlow Inventory

Retrieves an existing stock transfer from inFlow Inventory.

## Endpoint

- **Method:** `GET`
- **Path:** `/stock-transfers/:stockTransferId`
- **Base URL:** `https://cloudapi.inflowinventory.com/{companyId}`
- **Official documentation:** [Get Stock Transfer](https://cloudapi.inflowinventory.com/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stockTransferId` | path | `string` | yes | The unique identifier of the stock transfer to retrieve. |
