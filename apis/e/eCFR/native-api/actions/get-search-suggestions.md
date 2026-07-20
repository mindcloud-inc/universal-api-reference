# Get Search Suggestions with eCFR

Retrieves search suggestions for a query from eCFR.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/search/v1/suggestions`
- **Base URL:** `https://www.ecfr.gov`
- **Official documentation:** [Get Search Suggestions](https://www.ecfr.gov/developers/documentation/api/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Partial search text for suggestions. |
