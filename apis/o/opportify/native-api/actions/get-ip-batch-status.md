# Get IP Batch Status with Opportify

Retrieves the status of an IP batch job in Opportify.

## Endpoint

- **Method:** `GET`
- **Path:** `/ip/batch/:jobId`
- **Base URL:** `https://api.opportify.ai/insights/v1`
- **Official documentation:** [Get IP Batch Status](https://www.opportify.ai/docs/api/api-reference/get-ip-batch-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The unique identifier of the batch job to retrieve status for. |
