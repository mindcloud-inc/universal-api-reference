# Refresh Session Token with Week Plan

## Endpoint

- **Method:** `POST`
- **Path:** `https://backend-api.weekplan.net/sessions/token`
- **Base URL:** `https://api.weekplan.net/v2`
- **Official documentation:** [Refresh Session Token](https://weekplan.net/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `refreshToken` | body | `string` | yes | Week Plan refresh token used to mint a fresh access token. |
