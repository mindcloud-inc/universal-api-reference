# Click with Airtop

Clicks an element in a specific Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/click`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Click](https://docs.airtop.ai/api-reference/airtop-api/windows/click)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `windowId` | path | `string` | yes | — |
| `elementDescription` | body | `string` | yes | A natural language description of the element to click |
