# Unsubscribe from Scout with Yutori

Deletes a subscription from a scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/unsubscribe`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Unsubscribe from Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `method` | body | `string` | yes | — |
| `address` | body | `string` | no | — |
