# Scrape URL With Extended JSON with ScrapingAnt

Retrieves extended JSON page data from ScrapingAnt.

## Endpoint

- **Method:** `GET`
- **Path:** `/extended`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL With Extended JSON](https://docs.scrapingant.com/json-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape with extended JSON output. |
| `browser` | query | `boolean` | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | query | `number` | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. |
| `return_page_source` | query | `boolean` | no | Return server response data unaltered by browser rendering. Works only with browser=true. |
| `proxy_type` | query | `list<string>` | no | Proxy pool type. Supported values are datacenter and residential. Accepted values: `datacenter`, `residential`. |
| `proxy_country` | query | `string` | no | Two-letter proxy country code, such as US, GB, BR, or DE. |
| `wait_for_selector` | query | `string` | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. |
| `block_resource` | query | `list<string>` | no | Resource type to block while rendering, such as image, stylesheet, script, xhr, or fetch. Accepted values: `document`, `eventsource`, `fetch`, `font`, `image`, `manifest`, `media`, `other`, `script`, `stylesheet`, `texttrack`, `websocket`, `xhr`. |
