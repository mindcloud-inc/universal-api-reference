# List Episode Guest Cast with TVMaze Schedule

Retrieves guest cast for a TVMaze episode.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/{{id}}/guestcast`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Episode Guest Cast](https://www.tvmaze.com/api#episode-guest-cast)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze episode ID. |
