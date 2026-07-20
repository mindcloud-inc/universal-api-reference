# Get Shared Job with Deepset

Retrieves a shared job from a Deepset workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/workspaces/:workspace_id/shared_jobs/:shared_job_id`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Shared Job](https://docs.cloud.deepset.ai/docs/api/jobs/get-shared-job-api-v-2-workspaces-workspace-id-shared-jobs-shared-job-id-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared_job_id` | path | `string` | yes | deepset shared job ID. |
| `workspace_id` | path | `string` | yes | deepset workspace ID. |
