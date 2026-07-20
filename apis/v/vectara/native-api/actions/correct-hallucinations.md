# Correct Hallucinations with Vectara

Corrects hallucinations in generated text with Vectara.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/hallucination_correctors/correct_hallucinations`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Correct Hallucinations](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generated_text` | body | `string` | yes | Generated text to check and correct for hallucinations. |
| `documents[]` | body | `array<object>` | yes | Source document objects used for hallucination correction. |
| `model_name` | body | `string` | yes | Hallucination correction model name. |
| `query` | body | `string` | no | Optional query context for correction. |
