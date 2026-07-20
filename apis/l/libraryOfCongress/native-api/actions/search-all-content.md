# Search All Content with Library of Congress

Finds content across Library of Congress by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/`
- **Base URL:** `https://www.loc.gov`
- **Official documentation:** [Search All Content](https://www.loc.gov/apis/json-and-yaml/requests/endpoints/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Keyword search across loc.gov metadata and available full text. |
| `fa` | query | `string` | no | Optional loc.gov facet filters such as location:ohio or original-format:periodical\|subject:wildlife. |
| `at` | query | `string` | no | Optional response attributes to return, for example results, facets, or pagination. |
| `sb` | query | `string` | no | Optional sort field such as date, date_desc, title_s, or shelf_id. |
