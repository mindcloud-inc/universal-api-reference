# Search Companies with Implisense

Finds companies in Implisense API with filters and facets.

## Endpoint

- **Method:** `POST`
- **Path:** `/search`
- **Base URL:** `https://german-company-data.p.rapidapi.com`
- **Official documentation:** [Search Companies](https://docs.implisense.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Free-text company search query. |
| `from` | query | `number` | no | Result offset for search pagination. |
| `size` | query | `number` | no | Maximum number of results to return. |
| `explain` | query | `boolean` | no | Include explanation details in the search result. |
