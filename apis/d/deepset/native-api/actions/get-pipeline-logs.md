# Get Pipeline Logs with Deepset

Retrieves logs for a Deepset pipeline.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspaces/:workspace_name/pipelines/:pipeline_name/logs`
- **Base URL:** `https://api.cloud.deepset.ai`
- **Official documentation:** [Get Pipeline Logs](https://docs.cloud.deepset.ai/docs/api/main/get-pipeline-logs-api-v-1-workspaces-workspace-name-pipelines-pipeline-name-logs-get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipeline_name` | path | `string` | yes | deepset pipeline name. |
| `workspace_name` | path | `string` | yes | deepset workspace name. |
