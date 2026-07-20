# Start Sitemap with ScrapeGraphAI

Starts a sitemap extraction job in ScrapeGraphAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/sitemap`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Start Sitemap](https://docs.scrapegraphai.com/api-reference/endpoint/sitemap/start)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `headers` | body | `object` | no | Optional custom HTTP headers to send with the request. |
| `mock` | body | `boolean` | no | Return mock data instead of performing a live sitemap extraction. |
| `stealth` | body | `boolean` | no | Enable stealth mode to bypass bot protection. |
| `website_url` | body | `string` | yes | Website URL whose sitemap should be discovered and extracted. |
