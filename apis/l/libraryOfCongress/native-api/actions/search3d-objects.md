# Search 3D Objects with Library of Congress

Finds 3D objects in Library of Congress.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search 3D Objects](https://www.loc.gov/apis/json-and-yaml/requests/parameters/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Full-text search query. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
