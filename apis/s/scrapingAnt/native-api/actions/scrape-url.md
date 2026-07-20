# Scrape URL with ScrapingAnt

Retrieves scraped page HTML from ScrapingAnt.

## Endpoint

- **Method:** `GET`
- **Path:** `/general`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Scrape URL](https://docs.scrapingant.com/request-response-format)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape. |
| `browser` | query | `boolean` | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | query | `number` | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. |
| `return_page_source` | query | `boolean` | no | Return server response data unaltered by browser rendering. Works only with browser=true. |
| `proxy_type` | query | `list<string>` | no | Proxy pool type. Supported values are datacenter and residential. Accepted values: `datacenter`, `residential`. |
| `proxy_country` | query | `string` | no | Two-letter proxy country code, such as US, GB, BR, or DE. |
| `cookies` | query | `string` | no | Cookie header string to pass to the target site. |
| `js_snippet` | query | `string` | no | Base64-encoded JavaScript snippet to run after the page loads. Requires browser=true. |
| `wait_for_selector` | query | `string` | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. |
| `block_resource` | query | `list<string>` | no | Resource type to block while rendering, such as image, stylesheet, script, xhr, or fetch. Accepted values: `document`, `eventsource`, `fetch`, `font`, `image`, `manifest`, `media`, `other`, `script`, `stylesheet`, `texttrack`, `websocket`, `xhr`. |
