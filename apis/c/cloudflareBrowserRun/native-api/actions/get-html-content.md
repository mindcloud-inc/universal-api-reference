# Get HTML Content with Cloudflare Browser Run

Retrieves rendered HTML from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/content`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get HTML Content](https://developers.cloudflare.com/browser-rendering/rest-api/content-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
