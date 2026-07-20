# Get Bulk Job Status with SparrowDesk

Retrieves bulk job status from SparrowDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/status/{{jobId}}`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Get Bulk Job Status](https://developer.sparrowdesk.com/rest-api/endpoints/bulk/status/jobid/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Bulk job ID returned by Bulk Create Contacts. |
