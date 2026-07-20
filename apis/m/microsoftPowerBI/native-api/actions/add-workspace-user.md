# Add Workspace User with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Add Workspace User](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/add-group-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `identifier` | body | `string` | yes | The user, group, or app identifier to add to the workspace. |
| `principalType` | body | `list` | yes | The type of principal being added. |
| `groupUserAccessRight` | body | `list` | yes | The workspace access level to grant. |
