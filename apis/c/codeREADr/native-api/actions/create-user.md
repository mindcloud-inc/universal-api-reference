# Create User with CodeREADr

Creates a new app user in CodeREADr.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/`
- **Base URL:** `https://api.codereadr.com`
- **Official documentation:** [Create User](https://secure.codereadr.com/apidocs/Users.md#create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | CodeREADr username for the new user. |
| `password` | body | `string` | no | Required when username is not an email address. |
| `limit` | body | `string` | no | Optional device activation limit for the user. |
