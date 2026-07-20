# Get Daily Search Counts with eCFR

Retrieves daily search result counts from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/counts/daily`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Daily Search Counts](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text for daily counts. |
