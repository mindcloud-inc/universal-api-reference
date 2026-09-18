# Update User with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:userId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update User](https://api.gocanvas.com/api/v3/docs#update-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | — |
| `first_name` | body | `string` | no | — |
| `last_name` | body | `string` | no | — |
| `phone` | body | `string` | no | — |
| `enabled` | body | `boolean` | no | Set false to deactivate or true to reactivate. Reactivation requires an available seat. |
