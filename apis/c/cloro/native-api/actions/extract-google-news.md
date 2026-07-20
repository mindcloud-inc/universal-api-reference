# Extract Google News with Cloro

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/monitor/google/news`
- **Base URL:** `https://api.cloro.dev`
- **Official documentation:** [Extract Google News](https://docs.cloro.dev/api-reference/endpoint/monitor-google-news)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code for localized news results. |
| `device` | body | `string` | no | Device type for news results. |
| `query` | body | `string` | yes | The search query to execute on Google News. |
| `pages` | body | `number` | no | Number of news results pages to scrape. |
| `include` | body | `object` | no | Optional flags for additional Google News response data. |
| `include.html` | body | `boolean` | no | Include raw HTML response URLs. |
