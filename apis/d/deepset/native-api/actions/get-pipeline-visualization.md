# Get Pipeline Visualization with Deepset

Retrieves visualization data for a Deepset pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/visualization`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline Visualization](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-visualization-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-visualization-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
