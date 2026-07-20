# Update Role with Zammad

Updates an existing role in Zammad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/roles/:id`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Update Role](https://docs.zammad.org/en/latest/api/role.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Role ID. |
| `note` | body | `string` | yes | Role note. |
