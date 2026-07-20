# Get Job Status with Mindee

Retrieves a job status from Mindee.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/jobs/:job_id`
- **Base URL:** `https://api-v2.mindee.net`
- **Official documentation:** [Get Job Status](https://docs.mindee.com/integrations/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | UUID of the job to retrieve |
| `redirect` | query | `boolean` | no | Automatically redirect to the result URL |
