# Get Crawl Result with Cloudflare Browser Run

Retrieves crawl job results from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/crawl/:jobId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Crawl Result](https://developers.cloudflare.com/browser-rendering/rest-api/crawl-endpoint/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Crawl job ID returned by Create Crawl Job. |
