# Close Browser Session with Cloudflare Browser Run

Closes a browser session in Cloudflare Browser Run.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Close Browser Session](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID to close. |
