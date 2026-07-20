# Get Pipeline Stats with Deepset

Retrieves statistics for a Deepset pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/stats`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline Stats](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-stats-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-stats-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
