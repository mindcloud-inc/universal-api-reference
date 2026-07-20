# List Workspace Users with Microsoft Power BI

## Endpoint

- **Method:** `GET`
- **Path:** `groups/[:groupId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [List Workspace Users](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/get-group-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
