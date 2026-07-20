# Get User Group Item with SimpleKPI

Retrieves a user's group item from SimpleKPI.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:userId/groupitems/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Get User Group Item](https://support.simplekpi.com/Developers/UsersGroupItems)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The group item ID assigned to the user. |
| `userId` | path | `number` | no | The user ID. |
