# Count Search Results with eCFR

Retrieves the count of search results from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/count`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Count Search Results](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text to count. |
