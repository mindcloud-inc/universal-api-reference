# Search Prospecting Companies with Lusha Connect

Finds prospecting companies in Lusha Connect by filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/prospecting/company/search`
- **Base URL:** `https://api.lusha.com`
- **Official documentation:** [Search Prospecting Companies](https://docs.lusha.com/apis/openapi/prospecting-search-and-enrich/searchprospectingcompanies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pages` | body | `object` | no | Pagination settings for the prospecting company search. Lusha requires size to be at least 10. |
| `filters` | body | `object` | yes | Prospecting company filters object following the official Lusha schema. |
