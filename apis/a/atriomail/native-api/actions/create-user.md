# Create User with Atriomail

## Endpoint

- **Method:** `POST`
- **Path:** `/users`
- **Base URL:** `https://system.atriomail.com/api/v1`
- **Official documentation:** [Create User](https://system.atriomail.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user's email address. |
| `name` | body | `string` | yes | The user's full name. |
| `password` | body | `string` | yes | The user's password. |
