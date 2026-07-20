# Create room token with Digital Samba

Creates a room access token in Digital Samba.

## Endpoint

- **Method:** `POST`
- **Path:** `/rooms/:room/token`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Create room token](https://developer.digitalsamba.com/rest-api/#rooms-POSTapi-v1-rooms--room--token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `body` | body | `object` | no | JSON request body documented for this endpoint. |
| `ud` | body | `string` | no | External user identifier. |
| `u` | body | `string` | no | User name. |
| `initials` | body | `string` | no | Custom initials for user tiles. |
| `role` | body | `string` | no | Role ID or name. |
| `breakoutId` | body | `string` | no | Breakout room id. |
| `avatar` | body | `string` | no | The url of the user’s avatar image. |
| `nbf` | body | `number` | no | Not before. Unix timestamp before which token is not valid. You can also use a string date time. |
| `exp` | body | `number` | no | Token expiration. Unix timestamp after which token is not valid. You can also use number of minutes until token expiration, or a string date time. |
