# Create Realtime Session with Runway

Creates a realtime session in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/realtime_sessions`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Create Realtime Session](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `avatar` | body | `object` | yes | Avatar object using a runway-preset or custom avatar id. |
| `maxDuration` | body | `number` | no | Maximum session duration in seconds, between 10 and 300. |
| `model` | body | `string` | yes | Runway currently requires gwm1_avatars. |
| `personality` | body | `string` | no | Optional session personality override. |
| `startScript` | body | `string` | no | Optional opening script override for the session. |
