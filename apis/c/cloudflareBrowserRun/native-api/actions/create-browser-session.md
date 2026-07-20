# Create Browser Session with Cloudflare Browser Run

Creates a browser session in Cloudflare Browser Run.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Create Browser Session](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keep_alive` | query | `number` | no | Keep-alive time in milliseconds. |
| `lab` | query | `boolean` | no | Use the experimental browser. |
| `recording` | query | `boolean` | no | Enable browser recording. |
| `targets` | query | `boolean` | no | Include browser targets in the create session response. |
