# Create User with Umbrella

Creates a new user in Umbrella.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.umbrella.com/admin/v2/users`
- **Base URL:** `https://api.umbrella.com`
- **Official documentation:** [Create User](https://developer.cisco.com/docs/cloud-security/create-user/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The user's email address. |
| `firstname` | body | `string` | no | The user's first name. |
| `lastname` | body | `string` | no | The user's last name. |
| `password` | body | `string` | no | The user's password. |
| `roleId` | body | `string` | no | The Umbrella role ID. |
| `timezone` | body | `string` | no | A valid IANA timezone like America/New_York. |
