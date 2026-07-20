# Create Chat Prefix Completion (Beta) with DeepSeek

## Endpoint

- **Method:** `POST`
- **Path:** `/beta/chat/completions`
- **Base URL:** `https://api.deepseek.com`
- **Official documentation:** [Create Chat Prefix Completion (Beta)](https://api-docs.deepseek.com/guides/chat_prefix_completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `list` | yes | Model ID to use Accepted values: `deepseek-chat`, `deepseek-reasoner`. |
| `messages[]` | body | `array` | yes | Conversation messages; last message must be assistant with prefix=true |
| `temperature` | body | `number` | no | Sampling temperature (0-2) |
| `max_tokens` | body | `number` | no | Maximum tokens to generate |
| `top_p` | body | `number` | no | Nucleus sampling (0-1) |
| `stop[]` | body | `array<string>` | no | Stop sequences |
| `stream` | body | `boolean` | no | Enable streaming response |
| `stream_options.include_usage` | body | `boolean` | no | Include usage chunk when stream=true |
| `logprobs` | body | `boolean` | no | Whether to return log probabilities |
| `response_format.type` | body | `list` | no | Response format type Accepted values: `json_object`, `text`. |
| `frequency_penalty` | body | `number` | no | Penalize repeated tokens (-2 to 2) |
| `presence_penalty` | body | `number` | no | Penalize tokens already in text (-2 to 2) |
| `thinking.type` | body | `list` | no | Reasoning mode type Accepted values: `disabled`, `enabled`. |
| `tools[]` | body | `array<object>` | no | JSON array of tool/function definitions for function calling |
| `tool_choice` | body | `string` | no | Tool choice mode or JSON object |
| `top_logprobs` | body | `number` | no | Number of most likely tokens to return (requires logprobs=true) |
| `messages[].role` | body | `list` | yes | Role of each message Accepted values: `assistant`, `system`, `tool`, `user`. |
| `messages[].content` | body | `string` | yes | Content of each message |
| `messages[].name` | body | `string` | no | Optional participant name |
| `messages[].tool_call_id` | body | `string` | no | Tool call ID for tool-role messages |
| `messages[].prefix` | body | `boolean` | no | Enable prefix completion on assistant message |
| `tools[].type` | body | `list` | yes | Tool type Accepted values: `function`. |
| `tools[].function` | body | `object` | yes | Function definition object |
| `tools[].function.name` | body | `string` | yes | Function name |
| `tools[].function.description` | body | `string` | no | Function description |
| `tools[].function.parameters` | body | `object` | no | JSON Schema describing function parameters |
| `tools[].function.strict` | body | `boolean` | no | Enable strict schema adherence |
| `response_format` | body | `object` | no | Response format object |
