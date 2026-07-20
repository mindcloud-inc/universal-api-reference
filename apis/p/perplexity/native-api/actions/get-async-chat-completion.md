# Get Async Chat Completion with Perplexity

Retrieves an async chat completion from Perplexity.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/async/sonar/:api_request`
- **Base URL:** `https://api.perplexity.ai`
- **Official documentation:** [Get Async Chat Completion](https://docs.perplexity.ai/api-reference/async-sonar-api-request-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_request` | path | `string` | yes | Async request ID to retrieve. |
