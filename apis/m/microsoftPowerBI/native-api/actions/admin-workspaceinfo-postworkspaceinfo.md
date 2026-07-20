# WorkspaceInfo PostWorkspaceInfo with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/workspaces/getInfo`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [WorkspaceInfo PostWorkspaceInfo](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-post-workspace-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetExpressions` | query | `boolean` | no | Whether to return dataset expressions (DAX and Mashup queries). If you set this parameter to true, you must fully enable metadata scanning in order for data to be returned. For more information, see Enable tenant settings for metadata scanning. |
| `datasetSchema` | query | `boolean` | no | Whether to return dataset schema (tables, columns and measures). If you set this parameter to true, you must fully enable metadata scanning in order for data to be returned. For more information, see Enable tenant settings for metadata scanning. |
| `datasourceDetails` | query | `boolean` | no | Whether to return data source details |
| `getArtifactUsers` | query | `boolean` | no | Whether to return user details for a Power BI item (such as a report or a dashboard) |
| `lineage` | query | `boolean` | no | Whether to return lineage info (upstream dataflows, tiles, data source IDs) |
| `workspaces[]` | body | `array<string>` | no | The required workspace IDs to be scanned (supports 1 to 100 workspace IDs) |
