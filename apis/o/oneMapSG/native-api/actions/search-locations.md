# Search Locations with OneMap SG

Finds locations in OneMap SG by search value.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/common/elastic/search`
- **Base URL:** `https://www.onemap.gov.sg`
- **Official documentation:** [Search Locations](https://www.onemap.gov.sg/apidocs/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchVal` | query | `string` | yes | The search text, address, postal code, or other lookup value to search in OneMap. |
| `returnGeom` | query | `string` | no | Whether to include geometry values in the search response. |
| `getAddrDetails` | query | `string` | no | Whether to include detailed address fields in the response. |
| `pageNum` | query | `number` | no | The results page number to return. |
