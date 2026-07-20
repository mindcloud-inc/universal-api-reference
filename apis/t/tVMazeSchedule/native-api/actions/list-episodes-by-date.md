# List Episodes By Date with TVMaze Schedule

Retrieves TVMaze episodes for a show by airdate.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}/episodesbydate`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Episodes By Date](https://www.tvmaze.com/api#episodes-by-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
| `date` | query | `string` | yes | Required TVMaze airdate in YYYY-MM-DD format. |
