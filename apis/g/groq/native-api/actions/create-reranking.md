# Create Reranking with Groq

Creates a reranking result in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/reranking`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Reranking](https://console.groq.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `query` | body | `string` | yes |
| `docs[]` | body | `array<string>` | yes |
| `instruction` | body | `string` | no |
