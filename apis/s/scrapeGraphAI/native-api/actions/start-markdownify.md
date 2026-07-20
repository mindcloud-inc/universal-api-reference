# Start Markdownify with ScrapeGraphAI

Starts a Markdownify conversion job in ScrapeGraphAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/markdownify`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Start Markdownify](https://docs.scrapegraphai.com/api-reference/endpoint/markdownify/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers` | body | `object` | no | Optional custom HTTP headers to send with the request. |
| `stealth` | body | `boolean` | no | Enable stealth mode to bypass bot protection. |
| `website_url` | body | `string` | yes | URL of the webpage to convert to Markdown. |
