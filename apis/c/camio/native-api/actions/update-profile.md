# Update Profile with Camio

Updates a profile in Camio.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user/profile`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Update Profile](https://api.camio.com/#create-a-profile)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Optional first name for the profile. |
| `last_name` | body | `string` | no | Optional last name for the profile. |
| `timezone` | body | `object` | no | Optional timezone object, for example `{ "timezone_offset": "-0300" }`. |
