# List Webhooks with Browse AI

Retrieves webhooks from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/webhooks`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [List Webhooks](https://developers.browse.ai/v2#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
