# Get LLM Result with Unit Preferences with Wolfram Alpha

Retrieves an LLM-ready Wolfram Alpha result with unit preferences.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/api/v1/llm-api`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get LLM Result with Unit Preferences](https://products.wolframalpha.com/llm-api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `units` | query | `string` | yes |
