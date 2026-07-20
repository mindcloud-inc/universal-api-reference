# Scrape Elements with Cloudflare Browser Run

Extracts page elements from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/scrape`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Scrape Elements](https://developers.cloudflare.com/browser-rendering/rest-api/scrape-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `elements[]` | body | `array<object>` | yes | Array of element selector objects to scrape, each with selector. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
