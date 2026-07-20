# Search Titles with OMDb

Finds titles in OMDb by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Search Titles](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Title text to search across OMDb. |
| `type` | query | `list` | no | Restrict search results to a movie, series, or episode. Accepted values: `episode`, `movie`, `series`. |
| `y` | query | `number` | no | Release year to narrow the search. |
| `page` | query | `number` | no | Results page number to return. |
