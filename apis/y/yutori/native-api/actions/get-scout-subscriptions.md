# Get Scout Subscriptions with Yutori

Retrieves subscriptions for a specific scout in Yutori.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scouting/tasks/:scout_id/subscriptions`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Get Scout Subscriptions](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
