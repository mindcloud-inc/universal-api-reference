# Reset password using the reset password hash with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/users/reset-password`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Reset password using the reset password hash](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | yes | The reset password hash |
| `password` | body | `string` | no | — |
