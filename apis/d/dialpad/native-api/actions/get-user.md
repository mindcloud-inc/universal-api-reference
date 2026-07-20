# Get User with Dialpad

Retrieves detailed user information from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Get User](https://developers.dialpad.com/reference/usersget)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The user's id. 'me' can be used if you are using a user level API key. |
