# List Season Episodes with TVMaze Schedule

Retrieves episodes for a TVMaze season.

## Endpoint

- **Method:** `GET`
- **Path:** `/seasons/{{id}}/episodes`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Season Episodes](https://www.tvmaze.com/api#season-episodes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Required TVmaze season ID. |
| `embed` | query | `string` | no | Optional embedded resource name, such as guestcast. |
