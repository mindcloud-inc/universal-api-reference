# List Show Images with TVMaze Schedule

Retrieves images for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/images`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Images](https://www.tvmaze.com/api#show-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
