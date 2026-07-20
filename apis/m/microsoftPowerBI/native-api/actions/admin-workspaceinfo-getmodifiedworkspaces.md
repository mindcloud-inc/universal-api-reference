# WorkspaceInfo GetModifiedWorkspaces with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/workspaces/modified`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [WorkspaceInfo GetModifiedWorkspaces](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-get-modified-workspaces)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `excludeInActiveWorkspaces` | query | `boolean` | no | Whether to exclude inactive workspaces |
| `excludePersonalWorkspaces` | query | `boolean` | no | Whether to exclude personal workspaces |
| `modifiedSince` | query | `date` | no | Last modified date (must be in ISO 8601 compliant UTC format) |
