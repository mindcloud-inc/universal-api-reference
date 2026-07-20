# Get Term with Markup AI

Retrieves term details from Markup AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/terminology/term-sets/:term_set_id/terms/:term_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Get Term](https://docs.markup.ai/api-reference/terminology/get-term)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the parent term set. |
| `term_id` | path | `string` | yes | UUID of the term. |
