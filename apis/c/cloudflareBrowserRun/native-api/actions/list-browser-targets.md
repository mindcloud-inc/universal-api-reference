# List Browser Targets with Cloudflare Browser Run

Lists browser targets in Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/list`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [List Browser Targets](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
