# Chat Completions with Kazm

Creates a chat completion in Kazm.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/chat/completions`
- **Base URL:** `https://api.lightningrod.ai/api/public/v1`
- **Official documentation:** [Chat Completions](https://docs.lightningrod.ai/rest-api/transform-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages` | body | `string` | no | Ordered chat messages array. |
| `model` | body | `string` | no | Model identifier to use for the chat completion. |
