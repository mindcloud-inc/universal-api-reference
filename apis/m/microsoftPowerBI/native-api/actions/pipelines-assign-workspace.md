# Assign Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `pipelines/[:pipelineId]/stages/[:stageOrder]/assignWorkspace`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Assign Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/pipelines/assign-workspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pipelineId` | path | `string` | yes | The deployment pipeline ID |
| `stageOrder` | path | `number` | yes | The deployment pipeline stage order. Development (0), Test (1), Production (2). |
| `workspaceId` | body | `string` | yes | The workspace ID. |
