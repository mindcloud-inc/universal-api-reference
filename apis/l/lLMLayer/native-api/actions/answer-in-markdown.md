# Answer in Markdown with LLMLayer

Retrieves a web-enhanced markdown answer from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/answer`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Answer in Markdown](https://docs.llmlayer.ai/api-reference/endpoint/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Question or prompt to answer in markdown. |
