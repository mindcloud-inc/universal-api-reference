# Start Job with NeverBounce

Updates an existing NeverBounce job by starting verification.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/start`
- **Base URL:** `https://api.neverbounce.com/v4.2`
- **Official documentation:** [Start Job](https://developers.neverbounce.com/reference/jobs-start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | body | `number` | yes | NeverBounce job identifier. |
| `run_sample` | body | `boolean` | no | Run the sample flow before processing the full job. |
| `allow_manual_review` | body | `boolean` | no | Allow NeverBounce manual review for this job run. |
