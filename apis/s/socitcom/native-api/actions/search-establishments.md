# Search Establishments with Société.com

Finds establishments in Société.com by company name.

## Endpoint

- **Method:** `GET`
- **Path:** `/etablissement/search`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Search Establishments](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-recherche-d-&eacute;tablissement-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `debut` | query | `string` | no | Result offset, starting at 1. |
| `nbrep` | query | `string` | no | Maximum results to return. |
| `nom` | query | `string` | no | Company name to search establishments for. |
