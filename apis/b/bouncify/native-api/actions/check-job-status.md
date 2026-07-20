# Check Job Status with Bouncify

Retrieves bulk email list job status from Bouncify.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk/:job_id`
- **Base URL:** `https://api.bouncify.io/v1`
- **Official documentation:** [Check Job Status](https://bouncify.io/docs/api-docs/bulk-validation/check-job-status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | Bulk verification job id to inspect. |
