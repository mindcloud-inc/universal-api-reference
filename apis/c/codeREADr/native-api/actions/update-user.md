# Update User with CodeREADr

Updates an existing app user in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Update User](https://secure.codereadr.com/apidocs/Users.md#edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | body | `string` | yes | CodeREADr user ID. |
| `username` | body | `string` | no | Updated CodeREADr username. |
| `password` | body | `string` | no | Optional new password for the user. |
| `limit` | body | `string` | no | Optional device activation limit for the user. |
