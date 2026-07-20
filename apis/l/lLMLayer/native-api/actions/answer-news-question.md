# Answer News Question with LLMLayer

Retrieves a news-based answer from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/answer`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Answer News Question](https://docs.llmlayer.ai/api-reference/endpoint/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Question or prompt to answer from news sources. |
