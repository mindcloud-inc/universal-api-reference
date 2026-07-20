# Autocomplete Companies with Société.com

Finds company autocomplete suggestions in Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/entreprise`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Autocomplete Companies](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-entreprises-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Maximum suggestions to return. |
| `offset` | query | `string` | no | Suggestion offset. |
| `q` | query | `string` | no | Search text. |
