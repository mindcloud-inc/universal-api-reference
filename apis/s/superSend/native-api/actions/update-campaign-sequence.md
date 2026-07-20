# Update Campaign Sequence with SuperSend

Updates a campaign sequence in SuperSend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/campaigns/{id}/sequence`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Update Campaign Sequence](https://docs.supersend.io/docs/campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Resource ID (UUID) |
| `nodes[]` | body | `array<object>` | no | — |
| `nodes[].id` | body | `string` | no | — |
| `nodes[].type` | body | `string` | no | — |
| `nodes[].data` | body | `object` | no | Node-specific data (varies by node type). **For emailNode:** use `subject_a` and `body_a` (required). Do NOT use bare `subject` or `body` — these fields are rejected. For A/B testing also include `subject_b`/`body_b`, `subject_c`/`body_c`, or `subject_d`/`body_d`. Example emailNode data: ```json { "type": 1, "label": "Email Step 1", "subject_a": "Hello {{first_name}}", "body_a": "<p>Your email body</p>", "wait": 1, "wait_unit": "days" } ``` |
| `nodes[].position` | body | `object` | no | — |
| `nodes[].position.x` | body | `number` | no | — |
| `nodes[].position.y` | body | `number` | no | — |
| `nodes[].style` | body | `object` | no | — |
| `nodes[].style.width` | body | `number` | no | — |
| `nodes[].style.height` | body | `number` | no | — |
| `nodes[].style.minWidth` | body | `number` | no | — |
| `nodes[].style.minHeight` | body | `number` | no | — |
| `edges[]` | body | `array<object>` | no | — |
| `edges[].id` | body | `string` | no | — |
| `edges[].source` | body | `string` | no | — |
| `edges[].sourceHandle` | body | `string` | no | — |
| `edges[].target` | body | `string` | no | — |
| `edges[].type` | body | `string` | no | Allowed values: buttonedge. Default: buttonedge. |
