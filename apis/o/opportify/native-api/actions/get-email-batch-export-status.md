# Get Email Batch Export Status with Opportify

Retrieves the status of an email batch export job in Opportify.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/batch/:jobId/exports/:exportId`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Get Email Batch Export Status](https://www.opportify.ai/docs/api/api-reference/get-email-batch-export-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the batch job. Format: uuid. Example: "84d22c8b-2cb6-4606-bfb1-361244a097e4". |
| `exportId` | path | `string` | yes | The unique identifier of the export job. Format: uuid. Example: "6f8d88ef-0896-4f69-90cd-7cc6ce5e6ddf". |
