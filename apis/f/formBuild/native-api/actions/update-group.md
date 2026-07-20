# Update Group with 123FormBuild

Updates an existing group in 123FormBuilder.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/{group_id}`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Update Group](https://www.123formbuilder.com/developer/api-v2-groups/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | The ID of the group you want to edit |
| `name` | body | `string` | no | Group name |
| `webhook_url` | body | `string` | no | The webhook URL for the group |
| `parent_id` | body | `number` | no | The ID of the parent group |
