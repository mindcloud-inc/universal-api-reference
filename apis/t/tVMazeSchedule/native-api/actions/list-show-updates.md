# List Show Updates with TVMaze Schedule

Retrieves show update timestamps from TVMaze.

## Endpoint

- **Method:** `GET`
- **Path:** `/updates/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [List Show Updates](https://www.tvmaze.com/api#show-updates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `since` | query | `string` | no | Optional update window: day, week, or month. |
