# Check Batch Validation Progress with Enrich.so

Retrieves batch email validation progress from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validation/batch/{batchId}`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Check Batch Validation Progress](https://doc.enrich.so/check-batch-validation-progress-27483193e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Batch ID returned by the batch validation submit action. |
