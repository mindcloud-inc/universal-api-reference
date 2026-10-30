# Assign User to Group with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:groupId/users`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Assign User to Group](https://api.gocanvas.com/api/v3/docs#assign-user-to-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | — |
| `id` | body | `number` | no | Provide this or Login. |
| `login` | body | `string` | no | User email address. Provide this or User ID. |
| `send_notification` | body | `boolean` | no | Notify the user, subject to notification settings. Defaults to false. |
