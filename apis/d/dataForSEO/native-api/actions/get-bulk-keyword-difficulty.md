# Get Bulk Keyword Difficulty with DataForSEO

Retrieves bulk keyword difficulty from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/bulk_keyword_difficulty/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Bulk Keyword Difficulty](https://docs.dataforseo.com/v3/dataforseo_labs-bulk_keyword_difficulty-live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords[]` | body | `array<string>` | yes | Keywords to score for difficulty in bulk. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
