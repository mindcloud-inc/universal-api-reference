# Get Browser Version with Cloudflare Browser Run

Retrieves browser version details from Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/browser/:sessionId/json/version`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [Get Browser Version](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Browser session ID. |
