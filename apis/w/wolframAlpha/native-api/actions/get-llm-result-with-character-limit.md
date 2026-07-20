# Get LLM Result with Character Limit with Wolfram Alpha

Retrieves an LLM-ready Wolfram Alpha result with a character limit.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/api/v1/llm-api`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get LLM Result with Character Limit](https://products.wolframalpha.com/llm-api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `maxchars` | query | `number` | yes |
