# Scrape URL with ScrapeOwl

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape`
- **Base URL:** `https://api.scrapeowl.com/v1`
- **Official documentation:** [Scrape URL](https://scrapeowl.com/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Target URL to scrape. |
| `elements[]` | body | `array<object>` | no | List of element selectors to extract from the webpage. |
| `html` | body | `boolean` | no | Return the page HTML when true. |
| `json_response` | body | `boolean` | no | Return JSON formatted output when true. |
| `return_headers` | body | `boolean` | no | Return headers from the target website server. |
| `return_cookies` | body | `boolean` | no | Return cookies from the target website server. |
| `headers` | body | `object` | no | HTTP headers to send to the target URL. |
| `cookies` | body | `string` | no | Cookie header value to send to the target URL. |
| `request_method` | body | `string` | no | Target request method: GET, POST, or PUT. |
| `post_data` | body | `string` | no | Data to send when requestMethod is POST or PUT. |
| `render_js` | body | `boolean` | no | Use a headless Chrome instance to execute JavaScript. |
| `wait_for` | body | `string` | no | Element selector or millisecond duration to wait before scraping. |
| `custom_js` | body | `string` | no | JavaScript to run on the page before extraction. |
| `screenshot` | body | `boolean` | no | Capture a screenshot; only works with render_js. |
| `block_resources` | body | `boolean` | no | Block CSS, images, and fonts while rendering JavaScript. |
| `reject_requests[]` | body | `array<string>` | no | Resource extensions or URLs to block during render_js scraping. |
| `premium_proxies` | body | `boolean` | no | Use residential premium proxies. |
| `country` | body | `string` | no | Residential proxy source country ISO code. |
| `session` | body | `string` | no | Sticky session value for reusing the same IP address. |
