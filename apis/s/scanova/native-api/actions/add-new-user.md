# Add New User with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/multi-users/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Add New User](https://docs.scanova.io/api-reference/endpoint/user_management/add)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the shared user |
| `email` | body | `string` | yes | Email address of the shared user |
| `access_level` | body | `list` | yes | Shared user access level id. Pre-defined access levels: Manager (1), Admin (2), Viewer (3) Accepted values: `1`, `2`, `3`. |
