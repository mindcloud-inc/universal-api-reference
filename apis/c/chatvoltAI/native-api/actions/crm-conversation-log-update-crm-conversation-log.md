# Update CRM Conversation Log with Chatvolt AI

Updates an existing CRM conversation log in Chatvolt AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/conversationLog/{logId}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update CRM Conversation Log](https://docs.chatvolt.ai/api-reference/endpoint/crm/conversation-log/update-crm-conversation-log)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `logId` | path | `string` | yes | The ID of the CRM conversation log to update. |
| `status` | body | `string` | no | The new status for the CRM conversation log. |
