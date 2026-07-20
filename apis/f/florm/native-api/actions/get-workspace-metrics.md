# Get Workspace Metrics with Florm

Retrieves metrics for a Florm workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/workspaces/:workspace_guid/metrics`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Get Workspace Metrics](https://api.florm.io/docs#/default/get_workspaces_metrics_v1_workspaces__workspace_guid__metrics_get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_guid` | path | `string` | yes | GUID of the Florm workspace. |
