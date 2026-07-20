# Get Autocomplete Suggestions with KLIPY

Retrieves autocomplete suggestions from KLIPY for a query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/:app_key/autocomplete/:q`
- **Base URL:** `https://api.klipy.com`
- **Official documentation:** [Get Autocomplete Suggestions](https://docs.klipy.com/search-suggestions-and-autocomplete/autocomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | path | `string` | yes |
| `limit` | query | `number` | no |
