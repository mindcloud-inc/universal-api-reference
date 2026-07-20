# Create Chat Completion Stream with SectorFlow.AI

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/{workspaceId}/completions/stream`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Create Chat Completion Stream](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The ID of the workspace. |
| `messages[]` | body | `array<object>` | yes | Messages for the streamed chat completion request. |
