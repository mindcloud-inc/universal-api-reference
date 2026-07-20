# Get Search Volume with DataForSEO

Retrieves keyword search volume from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/keywords_data/google_ads/search_volume/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Search Volume](https://docs.dataforseo.com/v3/keywords_data-google_ads-search_volume-live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keywords[]` | body | `array<string>` | yes | Keywords to get search volume for. |
| `location_name` | body | `string` | no | Full location name in hierarchical comma-separated format. |
| `language_code` | body | `string` | no | Two-letter ISO language code. |
