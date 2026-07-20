# Summarize Search Results with eCFR

Retrieves summary details for search results from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/summary`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Summarize Search Results](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text to summarize. |
