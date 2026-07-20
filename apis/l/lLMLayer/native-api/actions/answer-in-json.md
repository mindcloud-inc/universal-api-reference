# Answer in JSON with LLMLayer

Retrieves a web-enhanced JSON answer from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/answer`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Answer in JSON](https://docs.llmlayer.ai/api-reference/endpoint/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Question or prompt to answer in JSON. |
