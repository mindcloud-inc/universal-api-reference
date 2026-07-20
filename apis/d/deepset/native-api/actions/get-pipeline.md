# Get Pipeline with Deepset

Retrieves a Deepset pipeline by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
