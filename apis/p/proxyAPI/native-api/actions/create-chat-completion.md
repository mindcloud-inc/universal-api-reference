# Create Chat Completion with ProxyAPI

Creates a chat completion in ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Create Chat Completion](https://proxyapi.ru/docs/openai-text-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | OpenAI-compatible model id to run through ProxyAPI. |
| `messages[0].content` | body | `string` | yes | Prompt text for the chat completion. |
