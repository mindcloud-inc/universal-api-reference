# List Show AKAs with TVMaze Schedule

Retrieves aliases for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/akas`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show AKAs](https://www.tvmaze.com/api#show-akas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
