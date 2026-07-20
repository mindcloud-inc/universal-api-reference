# Create Group with 123FormBuild

Creates a new group in 123FormBuilder.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Create Group](https://www.123formbuilder.com/developer/api-v2-groups/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Group name |
| `webhook_url` | body | `string` | no | The webhook URL for the group |
| `parent_id` | body | `number` | no | The ID of the parent group |
