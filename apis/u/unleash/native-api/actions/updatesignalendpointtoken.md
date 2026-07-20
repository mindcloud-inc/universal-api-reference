# [Beta] Update A Signal Endpoint Token. with Unleash

Updates a signal endpoint token in Unleash.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/admin/signal-endpoints/{signalEndpointId}/tokens/{id}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [[Beta] Update A Signal Endpoint Token.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signalEndpointId` | path | `string` | yes | Required path parameter. |
| `body` | body | `object` | yes | Required JSON request body. |
| `id` | path | `string` | yes | Required path parameter. |
