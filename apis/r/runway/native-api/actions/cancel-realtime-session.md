# Cancel Realtime Session with Runway

Cancels a realtime session in Runway.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/realtime_sessions/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Cancel Realtime Session](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions~1%7Bid%7D/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the realtime session to cancel. |
