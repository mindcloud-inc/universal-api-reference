# Verify Refresh Token with Instant

Verifies an Instant refresh token.

## Endpoint

- **Method:** `POST`
- **Path:** `/runtime/auth/verify_refresh_token`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Verify Refresh Token](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refresh-token` | body | `string` | yes | Refresh token to verify. |
