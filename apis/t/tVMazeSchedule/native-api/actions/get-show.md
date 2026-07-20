# Get Show with TVMaze Schedule

Retrieves a show from TVMaze by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/shows/{{id}}`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Get Show](https://www.tvmaze.com/api#show-main-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze show ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as episodes, cast, nextepisode, or previousepisode. |
