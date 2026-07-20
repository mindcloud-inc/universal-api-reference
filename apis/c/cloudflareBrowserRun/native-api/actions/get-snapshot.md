# Get Snapshot with Cloudflare Browser Run

Retrieves a DOM snapshot from Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/snapshot`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Snapshot](https://developers.cloudflare.com/browser-rendering/rest-api/snapshot-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `screenshotOptions` | body | `object` | no | Puppeteer screenshot options for the snapshot screenshot. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
