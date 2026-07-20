# Count Response Input Tokens with Open AI

Counts response input tokens in Open AI.

## Endpoint

- **Method:** `POST`
- **Path:** `v1/responses/input_tokens`
- **Base URL:** `https://api.openai.com`
- **Official documentation:** [Count Response Input Tokens](https://developers.openai.com/api/reference/overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Input content to count tokens for. |
| `model` | body | `string` | yes | Model ID used to count input tokens. |
