# Create Chat Completion with DeepSeek

## Endpoint

- **Method:** `POST`
- **Path:** `/chat/completions`
- **Base URL:** `https://api.deepseek.com`
- **Official documentation:** [Create Chat Completion](https://api-docs.deepseek.com/api/create-chat-completion)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `list` | yes | Model ID to use Accepted values: `deepseek-chat`, `deepseek-reasoner`. |
| `messages[]` | body | `array` | yes | Conversation messages (at least one item) |
| `max_tokens` | body | `number` | no | Maximum tokens to generate |
| `temperature` | body | `number` | no | Sampling temperature (0-2) |
| `top_p` | body | `number` | no | Nucleus sampling threshold (0-1) |
| `frequency_penalty` | body | `number` | no | Penalize repeated tokens (-2 to 2) |
| `presence_penalty` | body | `number` | no | Penalize tokens already in text (-2 to 2) |
| `logprobs` | body | `boolean` | no | Whether to return log probabilities |
| `stop[]` | body | `array<string>` | no | Stop sequence string or JSON array of up to 16 sequences |
| `stream` | body | `boolean` | no | Enable streaming response |
| `stream_options.include_usage` | body | `boolean` | no | Include usage chunks before [DONE] when stream=true |
| `thinking.type` | body | `list` | no | Reasoning mode type Accepted values: `disabled`, `enabled`. |
| `response_format.type` | body | `list` | no | Response format type Accepted values: `json_object`, `text`. |
| `tools[]` | body | `array<object>` | no | JSON array of tool/function definitions for function calling |
| `tool_choice` | body | `string` | no | Tool choice mode or JSON object |
| `top_logprobs` | body | `number` | no | Number of most likely tokens to return (requires logprobs=true) |
| `messages[].role` | body | `list<string>` | yes | Role of each message Accepted values: `assistant`, `system`, `tool`, `user`. |
| `messages[].content` | body | `string` | yes | Content of each message |
| `messages[].name` | body | `string` | no | Optional participant name |
| `messages[].tool_call_id` | body | `string` | no | Tool call ID for tool-role messages |
| `tools[].type` | body | `list` | yes | Tool type Accepted values: `function`. |
| `tools[].function` | body | `object` | yes | Function definition object |
| `tools[].function.name` | body | `string` | yes | Function name |
| `tools[].function.description` | body | `string` | no | Function description |
| `tools[].function.parameters` | body | `object` | no | JSON Schema describing function parameters |
| `tools[].function.strict` | body | `boolean` | no | Enable strict schema adherence |
| `response_format` | body | `object` | no | Response format object |
