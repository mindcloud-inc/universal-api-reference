# Prompt Content with Airtop

Queries Airtop window content from a prompt. Deprecated; use Query a Page instead.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/prompt-content`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Prompt Content](https://docs.airtop.ai/api-reference/airtop-api/windows/prompt-content)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
| `prompt` | body | `string` | yes |
