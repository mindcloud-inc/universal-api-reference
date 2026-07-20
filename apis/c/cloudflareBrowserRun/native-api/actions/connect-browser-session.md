# Connect Browser Session with Cloudflare Browser Run

Retrieves browser session connection details from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Connect Browser Session](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID to connect to. |
| `keep_alive` | query | `number` | no | Keep-alive time in milliseconds when connecting to a browser session. |
| `lab` | query | `boolean` | no | Use the experimental browser. |
| `recording` | query | `boolean` | no | Enable browser recording. |
