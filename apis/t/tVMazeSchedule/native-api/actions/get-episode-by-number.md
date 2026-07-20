# Get Episode By Number with TVMaze Schedule

Retrieves a TVMaze episode by season and number.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/episodebynumber`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Get Episode By Number](https://www.tvmaze.com/api#episode-by-number)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
| `season` | query | `number` | yes | Required season number. |
| `number` | query | `number` | yes | Required episode number within the season. |
