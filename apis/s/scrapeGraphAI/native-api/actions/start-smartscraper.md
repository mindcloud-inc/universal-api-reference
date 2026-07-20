# Start SmartScraper with ScrapeGraphAI

Starts a SmartScraper extraction job in ScrapeGraphAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/smartscraper`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Start SmartScraper](https://docs.scrapegraphai.com/api-reference/endpoint/smartscraper/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cookies` | body | `object` | no | Optional cookies object for authenticated pages or session state. |
| `headers` | body | `object` | no | Optional custom HTTP headers to send with the request. |
| `mock` | body | `boolean` | no | Return mock data instead of performing a live extraction. |
| `number_of_scrolls` | body | `number` | no | Number of times to scroll for infinite-scroll pages before extraction. |
| `output_schema` | body | `object` | no | Optional schema object to structure the extracted output. |
| `plain_text` | body | `boolean` | no | Return plain text instead of structured JSON output. |
| `stealth` | body | `boolean` | no | Enable stealth mode to bypass bot protection. |
| `steps[]` | body | `array<string>` | no | Optional interaction steps to perform on the page before extraction. |
| `total_pages` | body | `number` | no | Number of pages to extract when pagination is needed. |
| `user_prompt` | body | `string` | yes | Natural language description of what to extract from the page. |
| `website_html` | body | `string` | no | Raw HTML content to process directly, mutually exclusive with Website URL and Website Markdown. |
| `website_markdown` | body | `string` | no | Raw Markdown content to process directly, mutually exclusive with Website URL and Website HTML. |
| `website_url` | body | `string` | yes | URL of the webpage to extract information from. |
