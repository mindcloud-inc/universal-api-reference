# Create User with Edoobox

Creates a new user in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/user`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create User](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gender` | body | `string` | no | User gender. |
| `first_name` | body | `string` | yes | User first name. |
| `last_name` | body | `string` | yes | User last name. |
| `language` | body | `string` | no | User language code. |
| `data_1` | body | `string` | no | Custom user data field 1. |
