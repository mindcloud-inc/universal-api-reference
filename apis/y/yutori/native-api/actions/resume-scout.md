# Resume Scout with Yutori

Resumes a paused scout in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scouting/tasks/:scout_id/resume`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Resume Scout](https://docs.yutori.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scout_id` | path | `string` | yes | The scout UUID. |
