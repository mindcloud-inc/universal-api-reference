# Update Group Tag with Pachca (Admin)

Updates an existing group tag in the Pachca Admin API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/group_tags/:id`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [Update Group Tag](https://dev.pachca.com/api/group-tags/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Pachca group tag ID. |
| `name` | body | `string` | yes | — |
