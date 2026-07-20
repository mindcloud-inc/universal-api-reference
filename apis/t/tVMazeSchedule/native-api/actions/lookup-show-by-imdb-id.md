# Lookup Show By IMDb ID with TVMaze Schedule

Finds a TVMaze show by IMDb ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Lookup Show By IMDb ID](https://www.tvmaze.com/api#show-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imdb` | query | `string` | yes | Required IMDb title ID, for example tt0944947. |
