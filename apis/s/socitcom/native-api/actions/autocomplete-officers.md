# Autocomplete Officers with Société.com

Finds officer autocomplete suggestions in Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/dirigeant`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Autocomplete Officers](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-dirigeants-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Maximum suggestions to return. |
| `offset` | query | `string` | no | Suggestion offset. |
| `q` | query | `string` | no | Search text. |
