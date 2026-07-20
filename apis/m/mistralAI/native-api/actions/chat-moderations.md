# Chat Moderations with Mistral AI

Creates chat moderation results in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/moderations`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Chat Moderations](https://docs.mistral.ai/api/endpoint/classifiers#operation-chat_moderations_v1_chat_moderations_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | ID of the model to use. |
| `input[]` | body | `array<object>` | yes | Conversation messages to moderate. |
