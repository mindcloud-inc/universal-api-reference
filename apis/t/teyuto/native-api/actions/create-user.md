# Create User with Teyuto

Creates a new user in Teyuto.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Create User](https://apidocs.teyuto.com/api-9259125)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_user_id` | body | `string` | no | External client identifier for the user |
| `email` | body | `string` | no | Email of the user to create |
| `password` | body | `string` | no | Password for the new user |
