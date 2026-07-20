# Create Chat Completion with Open AI

Creates a model response for the given chat conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/chat/completions`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Create Chat Completion](https://developers.openai.com/api/reference/resources/chat)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | — |
| `messages[].content` | body | `string` | yes | Send multiple values as a array. |
| `response_format.type` | body | `list<string>` | no | — |
| `messages[].role` | body | `list<string>` | yes | — |
| `model` | body | `list<string>` | no | — |
| `frequency_penalty` | body | `date` | no | Number between -2.0 and 2.0. Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim. |
| `messages[].name` | body | `string` | no | — |
| `presence_penalty` | body | `date` | no | Number between -2.0 and 2.0. Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics. |
| `response_format` | body | `object` | no | — |
| `temperature` | body | `date` | no | What sampling temperature to use, between 0 and 2. Higher values like 0.8 will make the output more random, while lower values like 0.2 will make it more focused and deterministic. We generally recommend altering this or top_p but not both. |
