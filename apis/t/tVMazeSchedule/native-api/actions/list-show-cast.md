# List Show Cast with TVMaze Schedule

Retrieves cast members for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/cast`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Cast](https://www.tvmaze.com/api#show-cast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
