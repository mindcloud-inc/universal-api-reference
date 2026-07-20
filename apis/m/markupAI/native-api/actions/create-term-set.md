# Create Term Set with Markup AI

Creates a new term set in Markup AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/terminology/term-sets`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Create Term Set](https://docs.markup.ai/api-reference/terminology/create-term-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instructions` | body | `string` | yes | Instructions that define the term set. |
| `domain_ids[]` | body | `array<string>` | no | Optional terminology domain IDs to associate with the term set. |
