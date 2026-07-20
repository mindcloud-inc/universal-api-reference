# Get Browser Target with Cloudflare Browser Run

Retrieves browser target details from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/list/:targetId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Browser Target](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
| `targetId` | path | `string` | yes | Chrome DevTools target ID. |
