# Create Async Chat Completion with Perplexity

Creates an async chat completion in Perplexity.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/async/sonar`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Create Async Chat Completion](https://docs.perplexity.ai/api-reference/async-sonar-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request` | body | `object` | yes | Chat completion request object to execute asynchronously. |
| `idempotency_key` | body | `string` | no | Optional key to prevent duplicate async requests. |
