# Companies Typeahead with DataForB2B

Retrieves company suggestions from DataForB2B.

## Endpoint

- **Method:** `GET`
- **Path:** `/typeahead/companies`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Companies Typeahead](https://docs.dataforb2b.ai/api-reference/typeahead-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Autocomplete query string. |
| `limit` | query | `number` | no | Maximum number of suggestions to return. |
