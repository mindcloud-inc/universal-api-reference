# Get Keyword Ideas with DataForSEO

Retrieves keyword idea data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/keyword_ideas/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Keyword Ideas](https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_ideas-live/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords[]` | body | `array<string>` | yes | Seed keywords used to generate new keyword ideas. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
