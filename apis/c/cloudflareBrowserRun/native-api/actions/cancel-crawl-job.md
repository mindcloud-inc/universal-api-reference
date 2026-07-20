# Cancel Crawl Job with Cloudflare Browser Run

Cancels a crawl job in Cloudflare Browser Run.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:accountId/browser-rendering/crawl/:jobId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Cancel Crawl Job](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Crawl job ID to cancel. |
