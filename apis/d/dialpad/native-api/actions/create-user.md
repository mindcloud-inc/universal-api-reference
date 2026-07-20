# Create User with Dialpad

Creates a new user in Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Create User](https://developers.dialpad.com/reference/userscreate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auto_assign` | body | `boolean` | no | If set to true, a number will be automatically assigned. |
| `email` | body | `string` | yes | The user's email. |
| `first_name` | body | `string` | no | The user's first name. |
| `last_name` | body | `string` | no | The user's last name. |
| `license` | body | `string` | no | The user's license type. This affects billing for the user. |
| `office_id` | body | `number` | yes | The user's office id. |
