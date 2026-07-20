# Delete Term Set with Markup AI

Deletes an existing term set from Markup AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/terminology/term-sets/:term_set_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Delete Term Set](https://docs.markup.ai/api-reference/terminology/delete-term-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the term set to delete. |
