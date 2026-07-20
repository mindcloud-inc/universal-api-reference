# Scroll with Airtop

Scrolls within a specific Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/scroll`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Scroll](https://docs.airtop.ai/api-reference/airtop-api/windows/scroll)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `scrollToElement` | body | `string` | no |
