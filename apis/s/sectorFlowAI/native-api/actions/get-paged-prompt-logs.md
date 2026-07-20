# Get Paged Prompt Logs with SectorFlow.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/prompt-logs/paged`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get Paged Prompt Logs](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageable` | query | `string` | no | Pagination information required by the API. |
| `q` | query | `string` | no | Optional prompt log search query. |
