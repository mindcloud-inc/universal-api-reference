# Monitor For Condition with Airtop

Monitors an Airtop window for a condition.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/monitor`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Monitor For Condition](https://docs.airtop.ai/api-reference/airtop-api/windows/monitor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `windowId` | path | `string` | yes | — |
| `condition` | body | `string` | yes | A natural language description of the condition to monitor for |
