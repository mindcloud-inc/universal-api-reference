# Search Notated Music with Library of Congress

Finds notated music in Library of Congress.

## Endpoint

- **Method:** `GET`
- **Path:** `/notated-music/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search Notated Music](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Full-text search query. |
| `fa` | query | `string` | no | Facet filters such as subject or original format. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
