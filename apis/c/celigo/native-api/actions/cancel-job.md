# Cancel Job with Celigo

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:jobId/cancel`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [Cancel Job](https://developer.celigo.com/api/api-reference/monitoring/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Parent flow-run job to cancel. Only queued, running or retrying jobs can be canceled. |
