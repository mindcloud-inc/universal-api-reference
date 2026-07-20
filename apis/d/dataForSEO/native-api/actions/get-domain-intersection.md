# Get Domain Intersection with DataForSEO

Retrieves domain intersection data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/domain_intersection/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Domain Intersection](https://docs.dataforseo.com/v3/dataforseo_labs-google-domain_intersection-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target1` | body | `string` | yes | Primary domain for the intersection analysis. |
| `target2` | body | `string` | yes | Comparison domain for the intersection analysis. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
