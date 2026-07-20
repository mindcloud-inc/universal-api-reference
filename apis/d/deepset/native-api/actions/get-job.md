# Get Job with Deepset

Retrieves a job from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/workspaces/:workspace_id/jobs/:job_id`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Job](https://docs.cloud.deepset.ai/docs/api/jobs/get-job-api-v-2-workspaces-workspace-id-jobs-job-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | path | `string` | yes | deepset job ID. |
| `workspace_id` | path | `string` | yes | deepset workspace ID. |
