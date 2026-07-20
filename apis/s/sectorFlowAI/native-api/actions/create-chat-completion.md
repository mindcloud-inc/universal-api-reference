# Create Chat Completion with SectorFlow.AI

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/{workspaceId}/completions`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Create Chat Completion](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The workspace UUID. |
| `messages[]` | body | `array<object>` | yes | Chat messages for the completion request. |
