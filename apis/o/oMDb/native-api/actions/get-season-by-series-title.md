# Get Season by Series Title with OMDb

Retrieves a season from OMDb by series title and season.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Season by Series Title](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `t` | query | `string` | yes | Series title to use for the season lookup. |
| `Season` | query | `number` | yes | Season number to return. |
