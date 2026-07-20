# Mark Scout Done with Yutori

Marks a Yutori scout as done and archives it.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/done`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Mark Scout Done](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
