# Get Markdown with Cloudflare Browser Run

Retrieves webpage Markdown from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/markdown`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Markdown](https://developers.cloudflare.com/browser-rendering/rest-api/markdown-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
