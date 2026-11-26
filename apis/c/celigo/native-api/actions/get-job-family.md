# Get Job Family with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/:jobId/family`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [Get Job Family](https://developer.celigo.com/api/api-reference/monitoring/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Job ID, typically a parent flow-run job. Returns the job with its child step jobs under children. |
