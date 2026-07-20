# Create Task with retailCRM

Creates a new task in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/create`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `site` | body | `list` | yes |
| `task.text` | body | `string` | yes |
| `task.commentary` | body | `string` | no |
| `task.datetime` | body | `string` | yes |
| `task.performerId` | body | `list` | yes |
