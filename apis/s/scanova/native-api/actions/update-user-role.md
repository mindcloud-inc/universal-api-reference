# Update User Role with Scanova

## Endpoint

- **Method:** `PATCH`
- **Path:** `/multi-users/{shared-user-id}/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Update User Role](https://docs.scanova.io/api-reference/endpoint/user_management/update-role)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shared-user-id` | path | `number` | yes | ID of the shared user |
| `access_level` | body | `list` | yes | New access level ID for the user. Pre-defined access levels: Manager (1), Admin (2), Viewer (3) Accepted values: `1`, `2`, `3`. |
