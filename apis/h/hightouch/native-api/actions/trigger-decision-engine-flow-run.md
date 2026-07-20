# Trigger Decision Engine Flow Run with Hightouch

Triggers a decision engine flow run in Hightouch.

## Endpoint

- **Method:** `POST`
- **Path:** `/decision-engine/flow/{flowId}/run`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [Trigger Decision Engine Flow Run](https://api.hightouch.io/api/swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flowId` | path | `string` | yes | The Decision Engine flow ID. |
