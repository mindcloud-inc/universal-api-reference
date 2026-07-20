# Add Dashboard in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/dashboards`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Add Dashboard in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/dashboards/add-dashboard-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `name` | body | `string` | yes | The dashboard name. |
