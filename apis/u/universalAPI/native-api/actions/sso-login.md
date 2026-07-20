# SSO Login with Universal API

Retrieves an SSO login URL from Universal API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/sso/login`
- **Base URL:** `https://api.prod.universalapi.io`
- **Official documentation:** [SSO Login](https://docs.universalapi.io/reference/login)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `redirectUri` | query | `string` | yes | Redirect URI used by the SSO login flow. |
