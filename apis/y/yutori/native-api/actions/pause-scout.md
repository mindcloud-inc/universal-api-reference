# Pause Scout with Yutori

Pauses an active scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/pause`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Pause Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
