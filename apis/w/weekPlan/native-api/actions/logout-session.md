# Logout Session with Week Plan

## Endpoint

- **Method:** `POST`
- **Path:** `https://backend-api.weekplan.net/sessions/logout`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Logout Session](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refreshToken` | body | `string` | yes | Week Plan refresh token to invalidate during logout. |
