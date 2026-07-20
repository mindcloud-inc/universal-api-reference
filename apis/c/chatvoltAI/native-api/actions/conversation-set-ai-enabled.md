# Enable/Disable AI for Conversation with Chatvolt AI

Enables or disables AI for a conversation in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/set-ai-enabled`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Enable/Disable AI for Conversation](https://docs.chatvolt.ai/api-reference/endpoint/conversation/set-ai-enabled)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation for which the AI state will be changed. |
| `enabled` | body | `boolean` | yes | Defines the new AI state. `true` to enable, `false` to disable. |
