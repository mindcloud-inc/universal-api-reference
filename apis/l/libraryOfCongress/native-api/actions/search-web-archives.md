# Search Web Archives with Library of Congress

Finds web archives in Library of Congress.

## Endpoint

- **Method:** `GET`
- **Path:** `/web-archives/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search Web Archives](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Full-text search query. |
| `fa` | query | `string` | no | Facet filters such as subject or original format. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
