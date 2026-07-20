# List Show Alternate Lists with TVMaze Schedule

Retrieves alternate lists for a TVMaze show.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/alternatelists`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Alternate Lists](https://www.tvmaze.com/api#show-alternate-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
