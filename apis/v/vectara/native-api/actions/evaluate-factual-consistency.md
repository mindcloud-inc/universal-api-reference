# Evaluate Factual Consistency with Vectara

Evaluates generated text for factual consistency in Vectara.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/evaluate_factual_consistency`
- **Base URL:** `https://api.vectara.io`
- **Official documentation:** [Evaluate Factual Consistency](https://docs.vectara.com/docs/rest-api/vectara-rest-api-v-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generated_text` | body | `string` | yes | Generated text to evaluate for factual consistency. |
| `source_texts[]` | body | `array<string>` | yes | Source passages used to verify the generated text. |
| `model_parameters` | body | `object` | no | Optional model parameters for factual consistency evaluation. |
