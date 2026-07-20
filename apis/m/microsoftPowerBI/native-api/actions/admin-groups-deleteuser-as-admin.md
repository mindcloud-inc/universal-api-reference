# Groups DeleteUserAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `DELETE`
- **Path:** `admin/groups/[:groupId]/users/[:user]`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups DeleteUserAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-delete-user-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID. |
| `user` | path | `string` | yes | The user principal name (UPN) of the user or group object Id of the group or app object Id of the service principal to delete. |
| `isGroup` | query | `boolean` | no | Whether a given user is a group or not. This parameter is required when user to delete is group. |
| `profileId` | query | `string` | no | The service principal profile ID to delete. |
