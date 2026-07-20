# Search Movies with OMDb

Finds movies in OMDb by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Search Movies](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Movie title text to search. |
| `y` | query | `number` | no | Release year to narrow the movie search. |
| `page` | query | `number` | no | Results page number to return. |
