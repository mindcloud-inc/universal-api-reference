# Get LLM Result with Assumption with Wolfram Alpha

Retrieves an LLM-ready Wolfram Alpha result with assumptions.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.wolframalpha.com/api/v1/llm-api`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get LLM Result with Assumption](https://products.wolframalpha.com/llm-api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assumption` | query | `string` | yes |
| `input` | query | `string` | yes |
