# Get PDF with Cloudflare Browser Run

Generates a webpage PDF in Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/pdf`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get PDF](https://developers.cloudflare.com/browser-rendering/rest-api/pdf-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html` | body | `string` | no | HTML content to render. Either HTML or URL must be set. |
| `url` | body | `string` | no | URL to navigate to. Either URL or HTML must be set. |
| `pdfOptions` | body | `object` | no | Puppeteer PDF options such as format, margins, landscape, scale, and printBackground. |
| `cacheTTL` | query | `number` | no | Cache TTL in seconds. Set 0 to disable cache. |
