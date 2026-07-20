# List Conversations by Date with Chatvolt AI

Retrieves conversations by date from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Conversations by Date](https://docs.chatvolt.ai/api-reference/endpoint/conversation/list-by-date)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | query | `string` | no | Agent ID to filter conversations. If 'null' (string), searches for conversations not assigned to any agent. Optional. |
| `createdAt` | query | `string` | no | Filters conversations created from this date/time (inclusive). Accepted formats include 'YYYY-MM-DD HH:mm:ss', 'YYYY-MM-DD HH:mm', 'YYYY-MM-DD', or a complete ISO 8601 format. Optional. |
| `status` | query | `string` | no | Filters conversations by status. Optional. |
