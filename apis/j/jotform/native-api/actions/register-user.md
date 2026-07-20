# Register User with Jotform

Registers a new user in Jotform.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/register`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [Register User](https://api.jotform.com/docs/#user-id-register-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address for the new account. |
| `name` | query | `string` | no | Display name for the new account. |
| `password` | query | `string` | yes | Password for the new Jotform account. |
| `username` | query | `string` | yes | Username for the new Jotform account. |
