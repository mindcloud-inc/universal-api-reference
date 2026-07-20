# List Show Seasons with TVMaze Schedule

Retrieves seasons for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/seasons`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Seasons](https://www.tvmaze.com/api#show-seasons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
