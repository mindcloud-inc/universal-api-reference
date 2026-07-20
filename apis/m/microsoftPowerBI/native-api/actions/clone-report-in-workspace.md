# Clone Report in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/reports/[:reportId]/Clone`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Clone Report in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/reports/clone-report-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The source Power BI workspace ID. |
| `reportId` | path | `string` | yes | The report ID to clone. |
| `name` | body | `string` | yes | The name for the cloned report. |
| `targetWorkspaceId` | body | `string` | no | Optional target workspace ID for the cloned report. |
| `targetModelId` | body | `string` | no | Optional target dataset ID for the cloned report. |
