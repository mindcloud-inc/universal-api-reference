# Delete User Group Item with SimpleKPI

Deletes a group item from a SimpleKPI user.

## Endpoint

- **Method:** `DELETE`
- **Path:** `users/:userId/groupitems/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Delete User Group Item](https://support.simplekpi.com/Developers/UsersGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The group item ID assigned to the user. |
| `userId` | path | `number` | no | The user ID. |
