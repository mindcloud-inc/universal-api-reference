# Login User with Jotform

Creates a user session in Jotform.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/login`
- **Base URL:** `https://api.jotform.com`
- **Official documentation:** [Login User](https://api.jotform.com/docs/#user-id-login-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access` | query | `string` | no | Access level for the generated API key (readOnly/full). |
| `appName` | query | `string` | no | App label for the generated API key. |
| `password` | query | `string` | yes | Jotform account password. |
| `username` | query | `string` | yes | Jotform account username. |
