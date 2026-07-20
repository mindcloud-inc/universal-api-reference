# Function-Calling Chat Completion with ProxyAPI

Creates a function-calling chat completion in ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Function-Calling Chat Completion](https://platform.openai.com/docs/api-reference/chat/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model id to run through ProxyAPI. |
| `messages[0].content` | body | `string` | yes | Prompt that should trigger the function tool call. |
