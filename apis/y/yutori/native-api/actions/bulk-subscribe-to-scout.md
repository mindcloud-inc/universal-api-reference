# Bulk Subscribe to Scout with Yutori

Creates email subscriptions for a scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/subscribe/bulk`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Bulk Subscribe to Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `emails[]` | body | `array<string>` | yes | — |
