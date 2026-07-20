# Get Title by Title with OMDb

Retrieves title details from OMDb by title.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Title by Title](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `t` | query | `string` | yes | Movie, series, or episode title to look up. |
| `y` | query | `number` | no | Release year to narrow the title lookup. |
| `type` | query | `list` | no | Restrict the lookup to a movie, series, or episode. Accepted values: `episode`, `movie`, `series`. |
| `plot` | query | `list` | no | Return the short or full plot. Accepted values: `full`, `short`. |
