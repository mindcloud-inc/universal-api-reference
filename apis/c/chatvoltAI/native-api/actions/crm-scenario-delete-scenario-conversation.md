# Remove Conversation from CRM Scenario with Chatvolt AI

Removes a conversation from a CRM scenario in Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/crm/scenario/{scenarioId}/conversation`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Remove Conversation from CRM Scenario](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/delete-scenario-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | The ID of the CRM scenario. |
| `conversationId` | query | `string` | yes | ID of the conversation to remove from the scenario. |
