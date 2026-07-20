# List Scenario Conversations with Chatvolt AI

Retrieves CRM scenario conversations from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/scenario/{scenarioId}/conversation`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [List Scenario Conversations](https://docs.chatvolt.ai/api-reference/endpoint/crm/scenario/list-scenario-conversations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenarioId` | path | `string` | yes | The ID of the CRM scenario. |
| `stepId` | query | `string` | no | The ID of a specific step to filter conversations. |
| `page` | query | `number` | no | The page number for pagination. |
| `limit` | query | `number` | no | The number of items per page for pagination. |
| `isCount` | query | `boolean` | no | If true, returns conversation counts instead of the conversation list. |
| `showInactiveConversations` | query | `boolean` | no | If true, includes conversations that are not marked as available. |
