# Update Referrer Playback Restriction with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/playback-restrictions/{PLAYBACK_RESTRICTION_ID}/referrer`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update Referrer Playback Restriction](https://www.mux.com/docs/api-reference/video/playback-restrictions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allowed_domains[]` | body | `array<string>` | yes | The allowed referrer domains. |
| `PLAYBACK_RESTRICTION_ID` | path | `string` | yes | The playback restriction ID. |
