# Get Browser Session Details with Cloudflare Browser Run

Retrieves browser session details from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/session/:sessionId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Browser Session Details](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
