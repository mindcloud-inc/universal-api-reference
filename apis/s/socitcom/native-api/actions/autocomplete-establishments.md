# Autocomplete Establishments with Société.com

Finds establishment autocomplete suggestions in Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/autocomplete/etablissement`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Autocomplete Establishments](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-&eacute;tablissements-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | query | `string` | no | Maximum suggestions to return. |
| `offset` | query | `string` | no | Suggestion offset. |
| `q` | query | `string` | no | Search text. |
