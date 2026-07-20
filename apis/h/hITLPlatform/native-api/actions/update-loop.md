# Update Loop with HITL Platform

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/loops/:id`
- **Base URL:** `https://api.hitl.sh/v1`
- **Official documentation:** [Update Loop](https://docs.hitl.sh/api-reference/loops/update-loop)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated loop description. |
| `icon` | body | `string` | no | Updated loop icon name. |
| `id` | path | `string` | yes | The unique identifier of the loop. |
| `name` | body | `string` | no | Updated loop name. |
