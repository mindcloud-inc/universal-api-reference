# [Beta] Create A Signal Endpoint Token For A Specific Signal Endpoint. with Unleash

Creates a signal endpoint token for a specific signal endpoint in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/admin/signal-endpoints/{signalEndpointId}/tokens`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Create A Signal Endpoint Token For A Specific Signal Endpoint.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Required JSON request body. |
| `signalEndpointId` | path | `string` | yes | Required path parameter. |
