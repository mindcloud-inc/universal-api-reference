# Invalidate Access Token with LoginRadius

Invalidates an access token in LoginRadius.

## Endpoint

- **Method:** `GET`
- **Path:** `/identity/v2/auth/access_token/invalidate`
- **Base URL:** `https://api.loginradius.com`
- **Official documentation:** [Invalidate Access Token](https://www.loginradius.com/docs/api/openapi/invalidate-access-token/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_token` | query | `string` | yes | Access Token to invalidate. |
| `preventRefresh` | query | `boolean` | no | Whether to prevent refresh-token based renewal. |
