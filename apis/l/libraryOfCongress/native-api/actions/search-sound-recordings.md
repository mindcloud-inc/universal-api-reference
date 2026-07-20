# Search Sound Recordings with Library of Congress

Finds sound recordings in Library of Congress.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search Sound Recordings](https://www.loc.gov/apis/json-and-yaml/requests/parameters/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Full-text search query. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
