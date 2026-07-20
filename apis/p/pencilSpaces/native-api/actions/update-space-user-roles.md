# Update Space User Roles with Pencil Spaces

## Endpoint

- **Method:** `PATCH`
- **Path:** `/spaces/:spaceId/updateUsers`
- **Base URL:** `https://apis.pencilapp.com/public/api`
- **Official documentation:** [Update Space User Roles](https://api.pencilspaces.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `modifyUsers[]` | body | `array<object>` | no | Users whose role should be changed. |
| `modifyUsers[].role` | body | `string` | no | The new role for the user. |
| `modifyUsers[].userId` | body | `string` | no | The user whose Space role should change. |
| `notifyInvitees` | body | `boolean` | no | Whether Pencil should notify changed users. |
| `spaceId` | path | `string` | yes | The Space whose membership you want to update. |
