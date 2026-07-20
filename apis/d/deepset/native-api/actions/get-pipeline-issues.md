# Get Pipeline Issues with Deepset

Retrieves issues for a Deepset pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/issues`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline Issues](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-issues-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-issues-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
