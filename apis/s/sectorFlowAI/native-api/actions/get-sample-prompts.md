# Get Sample Prompts with SectorFlow.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{workspaceId}/sample-prompts`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get Sample Prompts](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | The workspace UUID. |
| `limit` | query | `number` | no | Maximum number of prompts to retrieve. Defaults to 6. |
