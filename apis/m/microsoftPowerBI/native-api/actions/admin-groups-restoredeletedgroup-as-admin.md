# Groups RestoreDeletedGroupAsAdmin with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `admin/groups/[:groupId]/restore`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Groups RestoreDeletedGroupAsAdmin](https://learn.microsoft.com/en-us/rest/api/power-bi/admin/groups-restore-deleted-group-as-admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The workspace ID |
| `emailAddress` | body | `string` | yes | The email address of the owner of the group to be restored |
| `name` | body | `string` | no | The name of the group to be restored |
