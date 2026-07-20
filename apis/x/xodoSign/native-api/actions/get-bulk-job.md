# Get Bulk Job with Xodo Sign

Retrieves a bulk job from Xodo Sign.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_job/:bulkSendingJobId`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Get Bulk Job](https://eversign.com/api/documentation/methods#get-bulk-job-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bulkSendingJobId` | path | `number` | yes | The bulk sending job ID to retrieve. |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the bulk job. |
