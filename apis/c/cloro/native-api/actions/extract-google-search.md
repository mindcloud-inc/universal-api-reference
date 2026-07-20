# Extract Google Search with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/google`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Google Search](https://docs.cloro.dev/api-reference/endpoint/monitor-google)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code for localized search results. |
| `device` | body | `string` | no | Device type for search results. |
| `location` | body | `string` | no | Google canonical location name for city-level targeting. |
| `query` | body | `string` | yes | The search query to execute on Google. |
| `uule` | body | `string` | no | Pre-encoded Google UULE string for precise geo-targeting. |
| `pages` | body | `number` | no | Number of search result pages to scrape. |
| `include` | body | `object` | no | Optional flags for additional Google response data. |
| `include.html` | body | `boolean` | no | Include raw HTML response URLs. |
| `include.aioverview` | body | `object` | no | Request Google AI Overview data in the Google Search response. |
