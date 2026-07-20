# Unshare Group with 123FormBuild

Removes a user's access to a group in 123FormBuilder.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/{group_id}/unshare`
- **Base URL:** `https://api.123formbuilder.com/v2`
- **Official documentation:** [Unshare Group](https://www.123formbuilder.com/developer/api-v2-groups/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `number` | yes | The ID of the group |
| `subuser_id` | body | `number` | no | The ID of the subuser to unshare the group from |
| `subuser_email` | body | `string` | no | The email of the subuser to unshare the group from |
