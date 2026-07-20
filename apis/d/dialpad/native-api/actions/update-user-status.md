# Update User Status with Dialpad

Updates a user's status in Dialpad.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:id/status`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Update User Status](https://developers.dialpad.com/reference/usersupdate_status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The user's id. |
| `status_message` | body | `string` | no | The status message for the user. |
| `expiration` | body | `number` | no | The expiration of this status. None for no expiration. |
