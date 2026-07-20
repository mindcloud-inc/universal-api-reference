# Create User Group Item with SimpleKPI

Creates a group item for a SimpleKPI user.

## Endpoint

- **Method:** `POST`
- **Path:** `users/:userId/groupitems`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Create User Group Item](https://support.simplekpi.com/Developers/UsersGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | The group item ID to assign to the user. |
| `userId` | path | `number` | no | The user ID. |
