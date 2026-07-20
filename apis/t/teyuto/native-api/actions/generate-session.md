# Generate Session with Teyuto

Creates an authenticated session in Teyuto.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Generate Session](https://docs.teyuto.com/api/generate-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | User ID to generate a session for when using the API key flow. |
| `expiration` | body | `number` | no | Validity of the session in seconds. |
| `client_user_id` | body | `string` | no | Custom client user ID to associate with the session. |
| `email` | body | `string` | no | User email for the email/password session flow. |
| `password` | body | `string` | no | User password for the email/password session flow. |
