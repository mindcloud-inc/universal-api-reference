# Create Chat Completion with Vectara

Creates a chat completion in Vectara.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/llms/chat/completions`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Create Chat Completion](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model ID to use for the chat completion. |
| `messages[]` | body | `array<object>` | yes | Conversation messages array in OpenAI-compatible format. |
| `stream` | body | `boolean` | no | Whether to stream partial chat completion chunks. |
| `response_format` | body | `object` | no | Requested output format for the response. |
