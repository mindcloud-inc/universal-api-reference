# Open Browser Tab with Cloudflare Browser Run

Opens a new browser tab in Cloudflare Browser Run.

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/new`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Open Browser Tab](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
| `url` | query | `string` | no | Optional URL to open in the new browser tab. |
