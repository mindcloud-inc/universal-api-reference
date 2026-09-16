# Get Current User with BarTender

Retrieves the current user profile from BarTender Cloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/connect/userinfo`
- **Base URL:** `https://auth.{region}.bartendercloud.com`
- **Official documentation:** [Get Current User](https://auth.am1.bartendercloud.com/.well-known/openid-configuration)

## Requirements

- **OAuth scopes:** `openid profile`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `MindCloud/1.0` |
