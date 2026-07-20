# Create User with Zammad

Creates a new user in Zammad.

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Create User](https://docs.zammad.org/en/latest/api/user.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstname` | body | `string` | yes | User first name. |
| `lastname` | body | `string` | yes | User last name. |
| `email` | body | `string` | yes | User email address. |
| `login` | body | `string` | yes | Unique login for the user. |
