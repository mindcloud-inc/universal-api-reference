# Update Workspace User with Microsoft Power BI

## Endpoint

- **Method:** `PUT`
- **Path:** `groups/[:groupId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Update Workspace User](https://learn.microsoft.com/en-us/rest/api/power-bi/groups/update-group-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The Power BI workspace ID. |
| `identifier` | body | `string` | yes | The user, group, or app identifier whose workspace access should be updated. |
| `principalType` | body | `list` | yes | The principal type. |
| `groupUserAccessRight` | body | `list` | yes | The updated workspace access level. |
