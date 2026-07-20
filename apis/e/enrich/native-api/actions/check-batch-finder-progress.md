# Check Batch Finder Progress with Enrich.so

Retrieves batch email finder progress from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-finder/batch/{batchId}`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Check Batch Finder Progress](https://doc.enrich.so/check-batch-finder-progress-27483197e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID returned by the batch email finder submit action. |
