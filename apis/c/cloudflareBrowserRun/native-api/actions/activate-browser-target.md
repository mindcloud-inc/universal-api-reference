# Activate Browser Target with Cloudflare Browser Run

Activates a browser target in Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/activate/:targetId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Activate Browser Target](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
| `targetId` | path | `string` | yes | Chrome DevTools target ID to activate. |
