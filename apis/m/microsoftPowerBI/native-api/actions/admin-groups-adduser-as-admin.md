# Groups AddUserAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/groups/[:groupId]/users`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups AddUserAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-add-user-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `groupUserAccessRight` | body | `list` | yes | The access right (permission level) that a user has on the workspace |
| `identifier` | body | `string` | yes | Identifier of the principal |
| `principalType` | body | `list` | yes | The principal type |
| `displayName` | body | `string` | no | Display name of the principal |
| `emailAddress` | body | `string` | no | Email address of the user |
| `graphId` | body | `string` | no | Identifier of the principal in Microsoft Graph. Only available for admin APIs. |
| `profile` | body | `object` | no | A Power BI service principal profile. Only relevant for Power BI Embedded multi-tenancy solution. |
| `userType` | body | `string` | no | Type of the user. |
