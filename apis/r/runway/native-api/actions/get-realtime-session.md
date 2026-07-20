# Get Realtime Session with Runway

Retrieves a realtime session from Runway.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/realtime_sessions/[:id]`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Get Realtime Session](https://docs.dev.runwayml.com/api#tag/Realtime-Sessions/paths/~1v1~1realtime_sessions~1%7Bid%7D/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | UUID of the realtime session to retrieve. |
