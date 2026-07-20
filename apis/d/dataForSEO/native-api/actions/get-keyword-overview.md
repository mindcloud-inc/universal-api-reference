# Get Keyword Overview with DataForSEO

Retrieves keyword overview data from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/google/keyword_overview/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Keyword Overview](https://docs.dataforseo.com/v3/dataforseo_labs-google-keyword_overview-live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords[]` | body | `array<string>` | yes | Keywords to summarize in the overview response. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
