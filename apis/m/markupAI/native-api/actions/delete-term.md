# Delete Term with Markup AI

Deletes an existing term from Markup AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/terminology/term-sets/:term_set_id/terms/:term_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Delete Term](https://docs.markup.ai/api-reference/terminology/delete-term)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the parent term set. |
| `term_id` | path | `string` | yes | UUID of the term to delete. |
