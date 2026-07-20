# Connect DevTools Page with Cloudflare Browser Run

Retrieves DevTools page connection details from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/page/:targetId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Connect DevTools Page](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
| `targetId` | path | `string` | yes | Chrome DevTools target or page ID. |
