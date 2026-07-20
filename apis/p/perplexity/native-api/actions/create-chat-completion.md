# Create Chat Completion with Perplexity

Creates a chat completion in Perplexity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sonar`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Create Chat Completion](https://docs.perplexity.ai/api-reference/sonar-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Sonar model to use, for example sonar-pro. |
| `messages[]` | body | `array<object>` | yes | Conversation history array in OpenAI chat format. |
| `max_tokens` | body | `number` | no | Maximum number of completion tokens to generate. |
| `stream` | body | `boolean` | no | When true, returns a streaming SSE response. |
| `temperature` | body | `number` | no | Controls randomness in the response. |
| `disable_search` | body | `boolean` | no | When true, disables web search for this request. |
| `search_domain_filter[]` | body | `array<string>` | no | Limit search results to specific domains. |
| `search_language_filter[]` | body | `array<string>` | no | Filter search results by ISO 639-1 language code. |
| `search_recency_filter` | body | `string` | no | Filter by publication recency. |
| `reasoning_effort` | body | `string` | no | Controls how much effort the model spends on reasoning. |
| `language_preference` | body | `string` | no | ISO 639-1 language code for the preferred response language. |
