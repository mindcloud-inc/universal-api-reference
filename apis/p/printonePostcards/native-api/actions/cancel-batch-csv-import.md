# Cancel Batch CSV Import with Print.one Postcards

Cancels a batch CSV import in Print.one Postcards.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/batches/:batchId/csv/:csvId/cancel`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Cancel Batch CSV Import](https://api.print.one/docs/v2#operation/Batch/cancelCsvImport)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | The batch ID. |
| `csvId` | path | `string` | yes | The CSV import ID. |
