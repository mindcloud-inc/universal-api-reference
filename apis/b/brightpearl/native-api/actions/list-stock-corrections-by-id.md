# List Stock Corrections by ID with Brightpearl

## Endpoint

- **Method:** `GET`
- **Path:** `/warehouse-service/warehouse/:warehouseId/stock-correction/:stockCorrectionIds`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [List Stock Corrections by ID](https://api-docs.brightpearl.com/warehouse/stock-correction/get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `warehouseId` | path | `number` | yes | — |
| `stockCorrectionIds` | path | `string` | yes | A single ID, comma-separated IDs, or ranges. Maximum 200 IDs. |
