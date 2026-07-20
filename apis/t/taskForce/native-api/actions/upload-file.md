# Upload File with TaskForce

Uploads a file to TaskForce.

## Endpoint

- **Method:** `POST`
- **Path:** `/upload`
- **Base URL:** `https://www.task-force.app/api`
- **Official documentation:** [Upload File](https://task-force.app/skill.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `file` | yes |
