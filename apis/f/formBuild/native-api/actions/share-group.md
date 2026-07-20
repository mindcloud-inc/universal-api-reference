# Share Group with 123FormBuild

Shares a group in 123FormBuilder with a user.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/{group_id}/share`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Share Group](https://www.123formbuilder.com/developer/api-v2-groups/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | The ID of the group |
| `subuser_id` | body | `number` | no | The ID of the subuser to share the group with |
| `subuser_email` | body | `string` | no | The email of the subuser to share the group with |
