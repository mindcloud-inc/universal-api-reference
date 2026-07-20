# Update Term Set with Markup AI

Updates an existing term set in Markup AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/terminology/term-sets/:term_set_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Update Term Set](https://docs.markup.ai/api-reference/terminology/update-term-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the term set to update. |
| `instructions` | body | `string` | no | Updated instructions for the term set. |
| `domain_ids[]` | body | `array<string>` | no | Updated terminology domain IDs for the term set. |
