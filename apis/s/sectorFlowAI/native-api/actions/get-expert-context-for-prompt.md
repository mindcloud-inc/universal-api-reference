# Get Expert Context For Prompt with SectorFlow.AI

## Endpoint

- **Method:** `POST`
- **Path:** `/plus/{plusId}/context-for-prompt`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get Expert Context For Prompt](https://docs.sectorflowai.com/reference/sectorplus-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plusId` | path | `string` | yes | The expert UUID. |
| `content` | body | `string` | yes | Prompt content to use for retrieving expert context. |
