# Move Conversation to CRM Step with Chatvolt AI

Moves a conversation to a CRM step in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/step/move`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Move Conversation to CRM Step](https://docs.chatvolt.ai/api-reference/endpoint/crm/step/move-step)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | body | `string` | yes | ID of the conversation to move. |
| `scenarioId` | body | `string` | no | ID of the CRM scenario. Required if `destStepId` is not provided or to specify context for `destStepIndex`. |
| `destStepId` | body | `string` | no | ID of the destination CRM step. If provided, `scenarioId` (if also provided) must match the step's scenario. |
| `destStepIndex` | body | `number` | no | Index of the destination step within the scenario (used with `scenarioId` if `destStepId` is not provided). |
| `shouldSendInitialMessage` | body | `boolean` | no | Whether to send the initial message of the destination step. |
