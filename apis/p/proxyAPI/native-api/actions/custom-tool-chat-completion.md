# Custom-Tool Chat Completion with ProxyAPI

Creates a custom-tool chat completion in ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Custom-Tool Chat Completion](https://platform.openai.com/docs/api-reference/chat/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model id that supports custom-tool chat completions when the account has sufficient balance. |
| `messages[0].content` | body | `string` | yes | Prompt that should trigger the custom tool call. |
