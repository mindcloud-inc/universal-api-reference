# Wait for Job with CloudConvert

Waits for a CloudConvert job to finish.

## Endpoint

- **Method:** `GET`
- **Path:** `https://sync.api.cloudconvert.com/v2/jobs/:id/wait`
- **Base URL:** `https://api.cloudconvert.com/v2`
- **Official documentation:** [Wait for Job](https://cloudconvert.com/docs/api-reference/jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CloudConvert job ID. |
