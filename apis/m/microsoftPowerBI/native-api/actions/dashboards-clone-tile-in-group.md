# Clone Tile In Group with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/dashboards/[:dashboardId]/tiles/[:tileId]/Clone`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Clone Tile In Group](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/clone-tile-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `dashboardId` | path | `string` | yes | The dashboard ID |
| `tileId` | path | `string` | yes | The tile ID |
| `targetDashboardId` | body | `string` | yes | The target dashboard ID |
| `positionConflictAction` | body | `object` | no | Optional. A parameter for specifying an action in case of a position conflict. If there's a conflict and this parameter isn't provided, then the default value Tail will be applied. If there's no conflict, then the cloned tile will have the same position as in the source. |
| `targetModelId` | body | `string` | no | Optional. A parameter for specifying a target model ID. When cloning a tile linked to a dataset, pass the target model ID to rebind the new tile to a different dataset. |
| `targetReportId` | body | `string` | no | Optional. A parameter for specifying a target report ID. When cloning a tile linked to a report, pass the target report ID to rebind the new tile to a different report. |
| `targetWorkspaceId` | body | `string` | no | Optional. A parameter for specifying a target workspace ID. An empty GUID (00000000-0000-0000-0000-000000000000) indicates **My workspace**. If this parameter isn't provided, the tile will be cloned within the same workspace as the source tile. |
