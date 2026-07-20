# Get IP Batch Export Status with Opportify

Retrieves the status of an IP batch export job in Opportify.

## Endpoint

- **Method:** `GET`
- **Path:** `/ip/batch/:jobId/exports/:exportId`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Get IP Batch Export Status](https://www.opportify.ai/docs/api/api-reference/get-ip-batch-export-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the batch job. Format: uuid. Example: "52b36b1f-0c21-41fa-8a4f-423d25a9a8e2". |
| `exportId` | path | `string` | yes | The unique identifier of the export job. Format: uuid. Example: "3b90d156-a0d8-4630-8230-f59e9a4e9e33". |
