# Update Batch with Print.one Postcards

Updates an existing batch in Print.one Postcards.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/batches/:batchId`
- **Base URL:** `https://api.print.one`
- **Official documentation:** [Update Batch](https://api.print.one/docs/v2#operation/Batch/updateBatch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID to update |
| `ready` | body | `string` | no | When true, send the batch as soon as requirements are met |
| `ready` | body | `boolean` | yes | When true, send the batch as soon as requirements are met |
| `requiredCount` | body | `number` | yes | Minimum number of orders required before the batch is sent |
