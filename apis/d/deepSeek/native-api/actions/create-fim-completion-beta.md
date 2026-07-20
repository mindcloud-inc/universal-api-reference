# Create FIM Completion (Beta) with DeepSeek

## Endpoint

- **Method:** `POST`
- **Path:** `/beta/completions`
- **Base URL:** `https://api.deepseek.com`
- **Official documentation:** [Create FIM Completion (Beta)](https://api-docs.deepseek.com/api/create-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The prefix text to complete |
| `suffix` | body | `string` | no | Text that comes after the completion |
| `max_tokens` | body | `number` | no | Maximum tokens to generate |
| `temperature` | body | `number` | no | Sampling temperature (0-2) |
| `top_p` | body | `number` | no | Nucleus sampling (0-1) |
| `frequency_penalty` | body | `number` | no | Penalize repeated tokens (-2 to 2) |
| `presence_penalty` | body | `number` | no | Penalize tokens already present (-2 to 2) |
| `logprobs` | body | `number` | no | Number of top log probabilities to return |
| `stop[]` | body | `array<string>` | no | Stop sequences |
| `stream` | body | `boolean` | no | Enable streaming response |
| `stream_options.include_usage` | body | `boolean` | no | Include usage chunk when stream=true |
| `echo` | body | `boolean` | no | Echo back the prompt in the completion response |
