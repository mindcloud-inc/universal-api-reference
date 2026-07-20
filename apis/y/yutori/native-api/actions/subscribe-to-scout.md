# Subscribe to Scout with Yutori

Creates a subscription for a scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/subscribe`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Subscribe to Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `method` | body | `string` | yes | — |
| `address` | body | `string` | no | — |
