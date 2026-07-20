# Locations Typeahead with DataForB2B

Retrieves location suggestions from DataForB2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/typeahead/locations`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Locations Typeahead](https://docs.dataforb2b.ai/api-reference/typeahead-locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Autocomplete query string. |
| `limit` | query | `number` | no | Maximum number of suggestions to return. |
