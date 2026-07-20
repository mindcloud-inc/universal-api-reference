# Search Single Show With Episodes with TVMaze Schedule

Finds a single TVMaze show by name with episodes.

## Endpoint

- **Method:** `GET`
- **Path:** `/singlesearch/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Search Single Show With Episodes](https://www.tvmaze.com/api#show-single-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Show name query to search for. |
