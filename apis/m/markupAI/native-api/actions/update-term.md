# Update Term with Markup AI

Updates an existing term in Markup AI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/terminology/term-sets/:term_set_id/terms/:term_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Update Term](https://docs.markup.ai/api-reference/terminology/update-term)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the parent term set. |
| `term_id` | path | `string` | yes | UUID of the term to update. |
| `term` | body | `string` | yes | Updated term value. |
| `type` | body | `string` | yes | Updated term type. |
