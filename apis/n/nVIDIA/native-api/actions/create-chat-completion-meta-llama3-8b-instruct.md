# Create Chat Completion (meta/llama3-8b-instruct) with NVIDIA

Creates a chat completion in NVIDIA using meta/llama3-8b-instruct.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://integrate.api.nvidia.com`
- **Official documentation:** [Create Chat Completion (meta/llama3-8b-instruct)](https://docs.api.nvidia.com/nim/reference/llm-apis)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Model name to use. |
| `messages[]` | body | `array<object>` | yes | Conversation messages array. |
