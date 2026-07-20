# Search Software and E-Resources with Library of Congress

Finds software and e-resources in Library of Congress.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search Software and E-Resources](https://www.loc.gov/apis/json-and-yaml/requests/parameters/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Full-text search query. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
