# Screen User with FraudLabs Pro

Screens a user for fraud in FraudLabs Pro.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/user/screen`
- **Base URL:** `https://api.fraudlabspro.com/`
- **Official documentation:** [Screen User](https://www.fraudlabspro.com/developer/api/screen-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The user email address. |
| `ip` | body | `string` | yes | The user IP address. |
