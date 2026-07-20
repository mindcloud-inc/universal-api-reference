# Log Request with PromptLayer Run Agent

Logs a request in PromptLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/log-request`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Log Request](https://docs.promptlayer.com/reference/log-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider` | body | `string` | yes | LLM provider for the logged request. |
| `model` | body | `string` | yes | Model name for the logged request. |
| `input` | body | `object` | yes | Prompt blueprint input payload. |
| `output` | body | `object` | yes | Prompt blueprint output payload. |
| `request_start_time` | body | `date` | yes | ISO timestamp for when the request started. |
| `request_end_time` | body | `date` | yes | ISO timestamp for when the request finished. |
| `api_type` | body | `string` | no | Provider API type such as chat-completions. |
| `metadata` | body | `object` | no | Optional metadata for request search and tracking. |
| `tags[]` | body | `array<string>` | no | Optional request tags. |
| `parameters` | body | `object` | no | Optional model parameters including structured outputs and reasoning settings. |
| `status` | body | `list` | no | Request status. |
| `error_type` | body | `list` | no | Optional categorized error type. |
| `error_message` | body | `string` | no | Optional detailed error message. |
| `prompt_input_variables` | body | `object` | no | Input variables for the associated prompt template. |
| `input_tokens` | body | `number` | no | Number of input tokens used by the request. |
| `output_tokens` | body | `number` | no | Number of output tokens used by the request. |
| `price` | body | `number` | no | USD cost for the request. |
| `function_name` | body | `string` | no | Optional function name for the logged request. |
| `score` | body | `number` | no | Optional request score from 0 to 100. |
| `prompt_name` | body | `string` | no | Optional prompt template name associated with the request. |
| `prompt_id` | body | `number` | no | Optional prompt template ID associated with the request. |
| `prompt_version_number` | body | `number` | no | Optional prompt version number associated with the request. |
