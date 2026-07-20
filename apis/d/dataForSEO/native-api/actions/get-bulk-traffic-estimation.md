# Get Bulk Traffic Estimation with DataForSEO

Retrieves bulk traffic estimates from DataForSEO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/dataforseo_labs/bulk_traffic_estimation/live.ai`
- **Base URL:** `https://api.dataforseo.com`
- **Official documentation:** [Get Bulk Traffic Estimation](https://docs.dataforseo.com/v3/dataforseo_labs-bulk_traffic_estimation-live/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targets[]` | body | `array<string>` | yes | Domains or URLs to estimate traffic for in bulk. |
| `location_name` | body | `string` | no | Location context for the DataForSEO Labs analysis. |
| `language_code` | body | `string` | no | Language code for the analysis context. |
