# Get Title Search Counts with eCFR

Retrieves search result counts by title from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/counts/titles`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Title Search Counts](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text for title counts. |
