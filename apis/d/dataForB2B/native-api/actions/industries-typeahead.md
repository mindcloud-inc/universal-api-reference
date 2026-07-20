# Industries Typeahead with DataForB2B

Retrieves industry suggestions from DataForB2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/typeahead/industries`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Industries Typeahead](https://docs.dataforb2b.ai/api-reference/typeahead-industries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Autocomplete query string. |
| `limit` | query | `number` | no | Maximum number of suggestions to return. |
