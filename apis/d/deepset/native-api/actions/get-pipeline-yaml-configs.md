# Get Pipeline YAML Configs with Deepset

Retrieves YAML configuration for a Deepset pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/yaml`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline YAML Configs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-yaml-configs-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-yaml-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
