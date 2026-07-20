# Lookup Show By TVRage ID with TVMaze Schedule

Finds a TVMaze show by TVRage ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/shows`
- **Base URL:** `https://api.tvmaze.com`
- **Official documentation:** [Lookup Show By TVRage ID](https://www.tvmaze.com/api#show-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tvrage` | query | `number` | yes | Required TVRage show ID. |
