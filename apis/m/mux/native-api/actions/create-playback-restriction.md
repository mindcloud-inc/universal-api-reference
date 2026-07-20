# Create Playback Restriction with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/playback-restrictions`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Create Playback Restriction](https://www.mux.com/docs/api-reference/video/playback-restrictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referrer` | body | `object` | yes | Referrer playback restriction configuration. |
| `user_agent` | body | `object` | yes | User agent playback restriction configuration. |
