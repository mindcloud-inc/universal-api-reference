# Acquire Browser Session with Cloudflare Browser Run

Retrieves an available browser session from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Acquire Browser Session](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keep_alive` | query | `number` | no | Keep-alive time in milliseconds when acquiring a new session. |
| `lab` | query | `boolean` | no | Use the experimental browser. |
| `recording` | query | `boolean` | no | Enable browser recording. |
