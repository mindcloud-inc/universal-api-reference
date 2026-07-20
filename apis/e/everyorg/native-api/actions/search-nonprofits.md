# Search Nonprofits with Every.org

Finds nonprofits in Every.org by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:searchTerm`
- **Base URL:** `https://partners.every.org/v0.2`
- **Official documentation:** [Search Nonprofits](https://docs.every.org/docs/endpoints/nonprofit-search#get-v02searchsearchterm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `causes` | query | `string` | no | Comma-separated causes to OR-filter search results. |
| `searchTerm` | path | `string` | yes | Search term to match nonprofit names and metadata. |
| `take` | query | `number` | no | Maximum number of results to return. Maximum 50. |
