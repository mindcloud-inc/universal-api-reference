# FIM Completion with Mistral AI

Creates a fill-in-the-middle completion in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/fim/completions`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [FIM Completion](https://docs.mistral.ai/api/endpoint/fim#operation-fim_completion_v1_fim_completions_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | ID of the model with FIM support to use. |
| `prompt` | body | `string` | yes | The text or code prefix to complete. |
| `suffix` | body | `string` | no | Optional suffix that the model should complete toward. |
| `temperature` | body | `number` | no | Sampling temperature for generation. |
| `top_p` | body | `number` | no | Nucleus sampling cutoff. |
| `max_tokens` | body | `number` | no | Maximum number of tokens to generate. |
| `min_tokens` | body | `number` | no | Minimum number of tokens to generate. |
| `stream` | body | `boolean` | no | Whether to stream partial progress. |
| `stop` | body | `string` | no | Stop generation when a token or one of the provided tokens is detected. |
| `random_seed` | body | `number` | no | Seed to use for deterministic random sampling. |
| `metadata` | body | `object` | no | Optional metadata object for the request. |
