# Assign Keys To Guardrail with OpenRouter

Assigns API keys to a guardrail in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/guardrails/:id/assignments/keys`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Assign Keys To Guardrail](https://openrouter.ai/docs/api/api-reference/guardrails/bulk-assign-keys-to-guardrail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Guardrail identifier. |
| `key_hashes[]` | body | `array<string>` | yes | API key hashes to assign to the guardrail. |
