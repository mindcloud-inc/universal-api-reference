# Get Episode by IMDb ID with OMDb

Retrieves an episode from OMDb by series IMDb ID, season, and episode.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Episode by IMDb ID](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Series IMDb ID to use for the episode lookup. |
| `Season` | query | `number` | yes | Season number that contains the episode. |
| `Episode` | query | `number` | yes | Episode number within the season. |
