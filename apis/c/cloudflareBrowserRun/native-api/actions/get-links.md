# Get Links with Cloudflare Browser Run

Retrieves webpage links from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/links`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Links](https://developers.cloudflare.com/browser-rendering/rest-api/links-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
