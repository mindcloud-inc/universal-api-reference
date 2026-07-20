# Get Access Token with Aqara Home for SG

Obtains an access token from Aqara Home for SG.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3.0/open/api`
- **Base URL:** `https://open-sg.aqara.com`
- **Official documentation:** [Get Access Token](https://opendoc.aqara.com/en/docs/developmanual/authManagement/aqaraauthMode.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.authCode` | body | `string` | yes | Verification code returned by Request Auth Code. |
| `data.account` | body | `string` | yes | The same Aqara account used to request the auth code. |
