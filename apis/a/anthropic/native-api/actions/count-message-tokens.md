# Count Message Tokens with Anthropic

Counts tokens in an Anthropic message request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messages/count_tokens`
- **Base URL:** `https://api.anthropic.com`
- **Official documentation:** [Count Message Tokens](https://platform.claude.com/docs/en/api/messages/count_tokens)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | The model that would complete your prompt. |
| `messages[]` | body | `array<object>` | yes | Input conversation messages. |
| `system` | body | `string` | no | System prompt content. |
