# Request Auth Code with Aqara Home for SG

Requests an authorization code from Aqara Home for SG.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3.0/open/api`
- **Base URL:** `https://open-sg.aqara.com`
- **Official documentation:** [Request Auth Code](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.account` | body | `string` | yes | Aqara account email or phone number that should receive the auth code. |
| `data.accessTokenValidity` | body | `string` | no | Optional token validity such as 1h, 1d, or 7d. |
