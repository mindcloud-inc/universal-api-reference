# Update Lead with Instantly

Updates an existing lead in Instantly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/leads/:id`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Update Lead](https://developer.instantly.ai/api-reference/lead/patch-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lead ID. |
| `first_name` | body | `string` | no | Updated first name. |
| `last_name` | body | `string` | no | Updated last name. |
