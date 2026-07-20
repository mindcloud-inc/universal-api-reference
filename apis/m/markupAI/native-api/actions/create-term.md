# Create Term with Markup AI

Creates a new term in Markup AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminology/term-sets/:term_set_id/terms`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Create Term](https://docs.markup.ai/api-reference/terminology/create-term)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term_set_id` | path | `string` | yes | UUID of the parent term set. |
| `term` | body | `string` | yes | Term value to create. |
| `type` | body | `string` | yes | Term type. |
