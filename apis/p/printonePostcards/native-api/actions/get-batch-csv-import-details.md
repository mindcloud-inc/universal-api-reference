# Get Batch CSV Import Details with Print.one Postcards

Retrieves batch CSV import details from Print.one Postcards.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/batches/:batchId/orders/csv/:csvId`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Get Batch CSV Import Details](https://api.print.one/docs/v2#operation/Batch/getCsvDetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | The batch ID. |
| `csvId` | path | `string` | yes | The CSV import ID. |
