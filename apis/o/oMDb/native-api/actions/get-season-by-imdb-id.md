# Get Season by IMDb ID with OMDb

Retrieves a season from OMDb by series IMDb ID and season.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Season by IMDb ID](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Series IMDb ID to use for the season lookup. |
| `Season` | query | `number` | yes | Season number to return. |
