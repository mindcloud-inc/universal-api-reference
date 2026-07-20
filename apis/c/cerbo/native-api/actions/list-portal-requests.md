# List Portal Requests with Cerbo

Retrieves queued patient portal requests from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/patients/:pt_id/portal/enqueued`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [List Portal Requests](https://docs.cer.bo/#tag/Patient-Portal/operation/showPortalRequests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | no | ID of patient |
| `request_type` | query | `string` | no | (COMING SOON) return only specific types of requests |
| `status` | query | `string` | no | (COMING SOON) return requests of a specific status (defaults to “open”) |
