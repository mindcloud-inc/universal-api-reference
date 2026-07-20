# Attach Task File with CoordinateHQ

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/task/:task_id/files/attach`
- **Base URL:** `https://app.coordinatehq.com/api/v1`
- **Official documentation:** [Attach Task File](https://app.coordinatehq.com/static/API_Documentation.html#project-pages)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `File` | body | `file` | yes |
| `task_id` | path | `string` | yes |
| `project_id` | path | `string` | yes |
