# Categories Typeahead with DataForB2B

Retrieves category suggestions from DataForB2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/typeahead/categories`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Categories Typeahead](https://docs.dataforb2b.ai/api-reference/typeahead-categories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Autocomplete query string. |
| `limit` | query | `number` | no | Maximum number of suggestions to return. |
