# Find Supported Locations with SearchAPI - Google Search

Finds supported Google search locations in SearchAPI.

## Endpoint

- **Method:** `GET`
- **Path:** `/locations`
- **Base URL:** `https://www.searchapi.io/api/v1`
- **Official documentation:** [Find Supported Locations](https://www.searchapi.io/docs/locations-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Location search text such as london or new york. |
| `limit` | query | `number` | no | Maximum number of locations to return. Defaults to 10 and can be up to 100. |
