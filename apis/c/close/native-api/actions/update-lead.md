# Update Lead with Close

Updates an existing lead in Close.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lead/:id/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [Update Lead](https://developer.close.com/resources/leads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique Lead ID. |
| `name` | body | `string` | no | Lead name. |
| `status_id` | body | `string` | no | Lead status ID. |
