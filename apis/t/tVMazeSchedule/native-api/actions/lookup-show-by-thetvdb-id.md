# Lookup Show By TheTVDB ID with TVMaze Schedule

Finds a TVMaze show by TheTVDB ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Lookup Show By TheTVDB ID](https://www.tvmaze.com/api#show-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thetvdb` | query | `number` | yes | Required TheTVDB show ID. |
