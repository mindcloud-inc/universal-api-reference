# Parallel Tool-Calling Chat with ProxyAPI

Creates a parallel tool-calling chat in ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Parallel Tool-Calling Chat](https://platform.openai.com/docs/api-reference/chat/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model id to run through ProxyAPI. |
| `messages[0].content` | body | `string` | yes | Prompt that should trigger multiple tool calls. |
