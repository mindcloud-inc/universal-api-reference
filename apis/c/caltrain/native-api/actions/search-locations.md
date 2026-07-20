# Search Locations with Caltrain

Finds Caltrain locations by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/location_autocomplete`
- **Base URL:** `https://www.caltrain.com`
- **Official documentation:** [Search Locations](https://www.caltrain.com/developer-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Location text to search for. |
