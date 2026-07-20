# Sign Out Session by Refresh Token with Instant

Signs out an Instant session by refresh token.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/sign_out`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Sign Out Session by Refresh Token](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh_token` | body | `string` | yes | Refresh token of the single session to revoke. |
