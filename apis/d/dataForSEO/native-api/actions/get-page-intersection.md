# Get Page Intersection with DataForSEO

Retrieves page intersection data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/page_intersection/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Page Intersection](https://docs.dataforseo.com/v3/dataforseo_labs-google-page_intersection-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pages` | body | `object` | yes | Object containing the pages to compare, keyed by numeric identifiers such as 1 and 2. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
| `intersection_mode` | body | `list<string>` | no | How the page sets should be combined for comparison. Accepted values: `intersect`, `union`. |
