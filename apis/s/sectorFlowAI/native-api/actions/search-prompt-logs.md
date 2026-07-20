# Search Prompt Logs with SectorFlow.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/prompt-logs`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Search Prompt Logs](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | no | End date for the log search. |
| `q` | query | `string` | no | Optional prompt log search query. |
| `startDate` | query | `string` | no | Start date for the log search. |
