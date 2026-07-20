# Search Pipeline with Deepset

Searches a Deepset pipeline with one or more queries.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/search`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Search Pipeline](https://docs.cloud.deepset.ai/docs/api/main/search-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-search-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queries[]` | body | `array<string>` | yes | Queries to run through the deployed pipeline. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
