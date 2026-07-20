# Get Location Suggestions with Prospeo

Finds location suggestions in Prospeo.

## Endpoint

- **Method:** `POST`
- **Path:** `/search-suggestions`
- **Base URL:** `https://api.prospeo.io`
- **Official documentation:** [Get Location Suggestions](https://prospeo.io/api-docs/search-suggestions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `location_search` | body | `string` | yes | Search query to find location suggestions. Minimum 2 characters. |
