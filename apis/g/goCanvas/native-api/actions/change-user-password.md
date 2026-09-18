# Change User Password with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/users/:userId/change_password`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Change User Password](https://api.gocanvas.com/api/v3/docs#change-user-password)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | — |
| `password` | body | `string` | yes | Must meet the company password policy. |
