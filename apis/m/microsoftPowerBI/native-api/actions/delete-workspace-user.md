# Delete Workspace User with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `groups/[:groupId]/users/[:user]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Delete Workspace User](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/delete-user-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `user` | path | `string` | yes | The user email address or object ID to remove from the workspace. |
