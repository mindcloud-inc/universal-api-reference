# Stream Chat Completion with ProxyAPI

Streams a chat completion from ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Stream Chat Completion](https://proxyapi.ru/docs/openai-text-generation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | OpenAI-compatible model id to run through ProxyAPI. |
| `messages[0].content` | body | `string` | yes | Prompt text for the streamed chat completion. |
