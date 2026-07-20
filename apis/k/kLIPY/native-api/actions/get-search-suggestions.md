# Get Search Suggestions with KLIPY

Retrieves search suggestions from KLIPY for a query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/search-suggestions/:q`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [Get Search Suggestions](https://docs.klipy.com/search-suggestions-and-autocomplete/search-suggestions)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | path | `string` | yes |
| `limit` | query | `number` | no |
