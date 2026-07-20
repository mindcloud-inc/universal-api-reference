# Search Series with OMDb

Finds series in OMDb by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/`
- **Base URL:** `https://www.omdbapi.com`
- **Official documentation:** [Search Series](https://www.omdbapi.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `s` | query | `string` | yes | Series title text to search. |
| `y` | query | `number` | no | Release year to narrow the series search. |
| `page` | query | `number` | no | Results page number to return. |
