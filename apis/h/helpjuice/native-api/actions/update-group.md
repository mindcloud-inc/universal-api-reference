# Update Group with Helpjuice

Updates an existing group in Helpjuice.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Group](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Helpjuice group id. |
| `name` | body | `string` | no | The Helpjuice group name. |
| `smart_load` | body | `boolean` | no | Whether the group uses smart loading. |
