# Update Group with Zammad

Updates an existing group in Zammad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Update Group](https://docs.zammad.org/en/latest/api/group.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group ID. |
| `note` | body | `string` | yes | Group note. |
