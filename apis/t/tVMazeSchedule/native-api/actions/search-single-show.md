# Search Single Show with TVMaze Schedule

Finds a single show in TVMaze by name.

## Endpoint

- **Method:** `GET`
- **Path:** `/singlesearch/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Search Single Show](https://www.tvmaze.com/api#show-single-search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Required show search query. |
| `embed` | query | `string` | no | Optional embedded resource name, such as episodes or cast. |
