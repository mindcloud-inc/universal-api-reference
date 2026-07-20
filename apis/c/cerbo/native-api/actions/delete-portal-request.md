# Delete Portal Request with Cerbo

Deletes a queued patient portal request from Cerbo.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/patients/:pt_id/portal/enqueued/:queue_request_id`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Delete Portal Request](https://docs.cer.bo/#tag/Patient-Portal/operation/deletePortalRequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pt_id` | path | `number` | no | ID of patient |
| `queue_request_id` | path | `number` | no | ID of queued request |
