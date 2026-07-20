# Get Bulk Job Status with Xodo Sign

Retrieves bulk job status from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_job/:bulkSendingJobId/status`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Get Bulk Job Status](https://eversign.com/api/documentation/methods#get-bulk-job-status-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkSendingJobId` | path | `number` | yes | The bulk sending job ID to retrieve. |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the bulk job. |
