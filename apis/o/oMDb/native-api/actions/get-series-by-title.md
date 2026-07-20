# Get Series by Title with OMDb

Retrieves series details from OMDb by title.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Series by Title](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `t` | query | `string` | yes | Series title to look up. |
| `y` | query | `number` | no | Release year to narrow the series lookup. |
| `plot` | query | `list` | no | Return the short or full plot. Accepted values: `full`, `short`. |
