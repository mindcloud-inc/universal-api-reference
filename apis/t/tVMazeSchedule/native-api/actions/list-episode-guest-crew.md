# List Episode Guest Crew with TVMaze Schedule

Retrieves guest crew for a TVMaze episode.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/{{id}}/guestcrew`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Episode Guest Crew](https://www.tvmaze.com/api#episode-guest-crew)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze episode ID. |
