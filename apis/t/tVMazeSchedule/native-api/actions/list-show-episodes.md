# List Show Episodes with TVMaze Schedule

Retrieves episodes for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/episodes`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Episodes](https://www.tvmaze.com/api#show-episode-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
| `specials` | query | `string` | no | Optional flag; set to 1 to include specials. |
