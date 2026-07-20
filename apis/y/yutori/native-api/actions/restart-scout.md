# Restart Scout with Yutori

Restarts an existing scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/restart`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Restart Scout](https://docs.yutori.com/reference/scout-restart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
