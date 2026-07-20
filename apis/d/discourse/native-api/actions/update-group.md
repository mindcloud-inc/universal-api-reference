# Update Group with Discourse

Updates an existing group in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Group](https://docs.discourse.org/#tag/Groups/operation/updateGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Group id. |
| `group.name` | body | `string` | yes | Group name. |
| `group.full_name` | body | `string` | no | Optional group display name. |
