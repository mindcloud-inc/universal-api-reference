# Create Chat Completion with Reka AI

Creates a chat completion in Reka AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/chat/completions`
- **Base URL:** `https://api.reka.ai`
- **Official documentation:** [Create Chat Completion](https://docs.reka.ai/chat/api-reference/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages` | body | `string` | yes | Chat messages array |
| `model` | body | `string` | yes | Model identifier |
