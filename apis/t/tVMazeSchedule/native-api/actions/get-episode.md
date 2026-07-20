# Get Episode with TVMaze Schedule

Retrieves an episode from TVMaze by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/episodes/{{id}}`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Get Episode](https://www.tvmaze.com/api#episode-main-information)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze episode ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as show. |
