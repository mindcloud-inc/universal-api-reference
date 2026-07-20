# Get Email Batch Status with Opportify

Retrieves the status of an email batch job in Opportify.

## Endpoint

- **Method:** `GET`
- **Path:** `/email/batch/:jobId`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Get Email Batch Status](https://www.opportify.ai/docs/api/api-reference/get-email-batch-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the batch job to retrieve status for. |
