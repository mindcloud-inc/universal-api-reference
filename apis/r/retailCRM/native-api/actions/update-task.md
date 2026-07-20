# Update Task with retailCRM

Updates an existing task in retailCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/edit`
- **Base URL:** `{accountUrl}/api/v5`

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `site` | body | `list` | yes |
| `task.text` | body | `string` | no |
| `task.commentary` | body | `string` | no |
| `task.datetime` | body | `string` | no |
| `task.performerId` | body | `list` | no |
| `task.complete` | body | `boolean` | no |
