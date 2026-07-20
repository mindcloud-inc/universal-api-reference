# Get Dubbing Job Status with Murf Dub

Retrieves a Murf Dub job status.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/murfdub/jobs/:job_id/status`
- **Base URL:** `https://api.murf.ai`
- **Official documentation:** [Get Dubbing Job Status](https://murf.ai/api/docs/api-reference/dubbing/jobs/get-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | The Murf Dub job ID to look up. |
