# Search Collection Items with Library of Congress

Finds items in a Library of Congress collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{collectionSlug}/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search Collection Items](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionSlug` | path | `string` | yes | The kebab-case loc.gov collection slug, such as civil-war-maps or baseball-cards. |
| `q` | query | `string` | no | Full-text search query. |
| `fa` | query | `string` | no | Facet filters such as subject or original format. |
| `at` | query | `string` | no | Comma-separated response sections to request. |
| `sb` | query | `string` | no | Sort order for search results. |
