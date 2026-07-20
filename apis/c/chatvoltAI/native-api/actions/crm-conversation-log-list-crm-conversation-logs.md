# List CRM Conversation Logs with Chatvolt AI

Retrieves CRM conversation logs from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/conversationLog`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List CRM Conversation Logs](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/list-crm-conversation-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | query | `string` | no | Filter logs by a specific Conversation ID. |
| `scenarioId` | query | `string` | no | Filter logs by a specific CRM Scenario ID. |
| `stepId` | query | `string` | no | Filter logs by a specific CRM Step ID. |
| `status` | query | `string` | no | Filter logs by status. |
| `page` | query | `number` | no | Page number for pagination. |
| `limit` | query | `number` | no | Number of logs per page. |
