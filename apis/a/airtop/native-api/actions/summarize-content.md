# Summarize Content with Airtop

Summarizes Airtop window content. Deprecated; use Query a Page instead.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/summarize-content`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Summarize Content](https://docs.airtop.ai/api-reference/airtop-api/windows/summarize-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | — |
| `windowId` | path | `string` | yes | — |
| `prompt` | body | `string` | no | Optional instructions that shape the summary output |
