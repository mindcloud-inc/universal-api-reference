# Get Ranked Keywords with DataForSEO

Retrieves ranked keyword data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/ranked_keywords/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Ranked Keywords](https://docs.dataforseo.com/v3/dataforseo_labs-google-ranked_keywords-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Domain to analyze for ranked keywords. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
| `include_subdomains` | body | `boolean` | no | Include subdomains of the target domain. |
