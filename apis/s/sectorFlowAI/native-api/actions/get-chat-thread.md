# Get Chat Thread with SectorFlow.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{workspaceId}/history/{threadId}`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get Chat Thread](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The workspace UUID. |
| `threadId` | path | `string` | yes | The chat thread UUID. |
