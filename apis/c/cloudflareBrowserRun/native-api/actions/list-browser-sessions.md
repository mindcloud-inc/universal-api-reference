# List Browser Sessions with Cloudflare Browser Run

Lists browser sessions in Cloudflare Browser Run.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/browser-rendering/devtools/session`
- **Base URL:** `https://api.cloudflare.com/client/v4`
- **Official documentation:** [List Browser Sessions](https://developers.cloudflare.com/api/resources/browser_rendering/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of browser sessions to return. |
| `offset` | query | `number` | no | Number of browser sessions to skip. |
