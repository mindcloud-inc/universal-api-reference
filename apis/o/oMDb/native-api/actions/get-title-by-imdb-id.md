# Get Title by IMDb ID with OMDb

Retrieves title details from OMDb by IMDb ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Get Title by IMDb ID](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | A valid IMDb ID, such as tt3896198. |
| `plot` | query | `list` | no | Return the short or full plot. Accepted values: `full`, `short`. |
