# Answer with Domain Filter with LLMLayer

Retrieves a domain-filtered answer from LLMLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/answer`
- **Base URL:** `https://api.llmlayer.dev`
- **Official documentation:** [Answer with Domain Filter](https://docs.llmlayer.ai/api-reference/endpoint/answer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Question or prompt to answer with domain filters. |
| `domain_filter[]` | body | `array<string>` | no | Include or exclude domains from the answer context. |
