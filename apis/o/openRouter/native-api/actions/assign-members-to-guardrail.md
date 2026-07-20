# Assign Members To Guardrail with OpenRouter

Assigns members to a guardrail in OpenRouter.

## Endpoint

- **Method:** `POST`
- **Path:** `/guardrails/:id/assignments/members`
- **Base URL:** `https://openrouter.ai/api/v1/`
- **Official documentation:** [Assign Members To Guardrail](https://openrouter.ai/docs/api/api-reference/guardrails/bulk-assign-members-to-guardrail)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Guardrail identifier. |
| `member_user_ids[]` | body | `array<string>` | yes | Member user IDs to assign to the guardrail. |
