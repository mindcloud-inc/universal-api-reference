# List Dashboards in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/dashboards`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Dashboards in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/get-dashboards-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
