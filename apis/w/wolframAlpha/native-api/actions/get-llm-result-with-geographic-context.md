# Get LLM Result with Geographic Context with Wolfram Alpha

Retrieves an LLM-ready Wolfram Alpha result with geographic context.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/api/v1/llm-api`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get LLM Result with Geographic Context](https://products.wolframalpha.com/llm-api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `location` | query | `string` | yes |
