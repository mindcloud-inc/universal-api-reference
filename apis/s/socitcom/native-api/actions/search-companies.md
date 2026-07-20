# Search Companies with Société.com

Finds companies in Société.com by company name.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/search`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [Search Companies](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-recherche-d-entreprise-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `debut` | query | `string` | no | Result offset, starting at 1. |
| `nbrep` | query | `string` | no | Maximum results to return. |
| `nom` | query | `string` | no | Company name to search. |
