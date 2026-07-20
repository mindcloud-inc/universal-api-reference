# Get Screenshot with Cloudflare Browser Run

Captures a webpage screenshot in Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/screenshot`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Screenshot](https://developers.cloudflare.com/browser-rendering/rest-api/screenshot-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `screenshotOptions` | body | `object` | no | Puppeteer screenshot options such as fullPage, clip, encoding, and type. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
