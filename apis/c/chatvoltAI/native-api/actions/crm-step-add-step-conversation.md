# Add Conversation to CRM Step with Chatvolt AI

Adds a conversation to a CRM step in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/step/conversation`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Add Conversation to CRM Step](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/add-step-conversation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | body | `string` | yes | ID of the conversation to add to the step. |
| `scenarioId` | body | `string` | no | ID of the CRM scenario. Required if `stepId` is not provided or if `stepIndex` is used. |
| `stepId` | body | `string` | no | ID of the specific CRM step. If provided, `scenarioId` and `stepIndex` are ignored for step identification. |
| `stepIndex` | body | `number` | no | Index of the step within the scenario (used with `scenarioId` if `stepId` is not provided). |
