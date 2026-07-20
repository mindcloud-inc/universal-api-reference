# Get Keywords for Site with DataForSEO

Retrieves keywords for a site from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/keywords_for_site/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Keywords for Site](https://docs.dataforseo.com/v3/dataforseo_labs-google-keywords_for_site-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | body | `string` | yes | Domain to analyze for site keywords. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
| `include_subdomains` | body | `boolean` | no | Include subdomains of the target domain. |
