# Retrieve Active Session with LoginRadius

Retrieves an active session from LoginRadius by access token.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/access_token/activesession`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Retrieve Active Session](https://www.loginradius.com/docs/api/openapi/get-active-session/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountid` | query | `string` | no | Account ID of the user. |
| `profileid` | query | `string` | no | Account ID of the user. |
| `token` | query | `string` | yes | Access token whose active session should be retrieved. |
