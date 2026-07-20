# Get Monitor with Browse AI

Retrieves a monitor from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/monitors/:monitorId`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [Get Monitor](https://developers.browse.ai/v2#tag/monitors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `monitorId` | path | `string` | yes | Unique monitor ID  You can find a monitor's ID by opening it on the dashboard and copying its ID in the browser address bar. |
