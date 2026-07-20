# Structured Chat Completion with ProxyAPI

Creates a structured chat completion in ProxyAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://openai.api.proxyapi.ru/v1`
- **Official documentation:** [Structured Chat Completion](https://platform.openai.com/docs/api-reference/chat/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | — |
| `messages[0].content` | body | `string` | yes | Prompt for the structured chat completion. |
