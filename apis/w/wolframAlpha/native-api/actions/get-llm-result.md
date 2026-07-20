# Get LLM Result with Wolfram Alpha

Retrieves an LLM-ready result from Wolfram Alpha.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/api/v1/llm-api`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get LLM Result](https://products.wolframalpha.com/llm-api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | query | `string` | yes | Natural-language query for the Wolfram\|Alpha LLM API. |
| `maxchars` | query | `number` | no | Maximum number of characters to return in the result. |
| `units` | query | `string` | no | Measurement system to use: metric or imperial. |
