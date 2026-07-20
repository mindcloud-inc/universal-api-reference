# Get DevTools Protocol Schema with Cloudflare Browser Run

Retrieves the DevTools protocol schema from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/protocol`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get DevTools Protocol Schema](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
