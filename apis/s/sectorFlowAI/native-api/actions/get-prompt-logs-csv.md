# Get Prompt Logs CSV with SectorFlow.AI

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/prompt-logs/csv`
- **Base URL:** `https://platform.sectorflow.ai/api/v1`
- **Official documentation:** [Get Prompt Logs CSV](https://docs.sectorflowai.com/reference/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Optional search query. |
| `startDate` | query | `string` | yes | Start date for the log export search. |
| `endDate` | query | `string` | yes | End date for the log export search. |
