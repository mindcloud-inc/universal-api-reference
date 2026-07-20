# Search Smartsheet with Smartsheet

Finds matching items in Smartsheet by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.smartsheet.com/2.0`
- **Official documentation:** [Search Smartsheet](https://developers.smartsheet.com/api/smartsheet/openapi/search/list-search)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `scopes` | query | `string` | no |
| `modifiedSince` | query | `date` | no |
| `include` | query | `string` | no |
| `location` | query | `string` | no |
