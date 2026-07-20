# Create Research Chat Completion with Reka AI

Creates a research chat completion in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Create Research Chat Completion](https://docs.reka.ai/research/api-reference/create-chat-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages` | body | `string` | yes | Chat messages array |
| `model` | body | `string` | yes | Model identifier |
