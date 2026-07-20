# Get Episode by Series Title with OMDb

Retrieves an episode from OMDb by series title, season, and episode.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Episode by Series Title](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `t` | query | `string` | yes | Series title to use for the episode lookup. |
| `Season` | query | `number` | yes | Season number that contains the episode. |
| `Episode` | query | `number` | yes | Episode number within the season. |
