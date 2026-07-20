# WorkspaceInfo GetScanStatus with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `admin/workspaces/scanStatus/[:scanId]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [WorkspaceInfo GetScanStatus](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/workspace-info-get-scan-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scanId` | path | `string` | yes | The scan ID, which is included in the response from the workspaces or the Admin - WorkspaceInfo PostWorkspaceInfo API call that triggered the scan. |
