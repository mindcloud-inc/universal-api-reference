# Update Scout with Yutori

Updates an existing scout in Yutori.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/scouting/tasks/:scout_id`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Update Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
| `query` | body | `string` | yes | — |
| `query_object` | body | `object` | yes | — |
| `display_name` | body | `string` | no | — |
| `user_timezone` | body | `string` | yes | — |
| `llm_output` | body | `object` | yes | — |
| `output_interval` | body | `number` | no | — |
| `next_output_timestamp` | body | `number` | no | — |
| `user_location` | body | `string` | no | — |
| `is_public` | body | `boolean` | no | — |
