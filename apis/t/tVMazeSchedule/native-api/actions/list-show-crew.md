# List Show Crew with TVMaze Schedule

Retrieves crew members for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/crew`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Crew](https://www.tvmaze.com/api#show-crew)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
