# Rotate User Credentials with Port API AI

Creates rotated credentials for a user in Port.

## Endpoint

- **Method:** `POST`
- **Path:** `/rotate-credentials/:user_email`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Rotate User Credentials](https://docs.port.io/api-reference/rotate-a-users-credentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_email` | path | `string` | yes | The Port user email. |
