# Load URL with Airtop

Loads a specified URL in an Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Load URL](https://docs.airtop.ai/api-reference/airtop-api/windows/load-url)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `url` | body | `string` | yes |
| `waitUntil` | body | `string` | no |
