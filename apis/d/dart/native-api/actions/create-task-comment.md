# Create Task Comment with Dart

Creates a task comment in Dart.

## Endpoint

- **Method:** `POST`
- **Path:** `/comments`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Create Task Comment](https://app.dartai.com/api/v0/public/docs/#/Comment/addTaskComment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `item.parentId` | body | `string` | no |
| `item.taskId` | body | `string` | no |
| `item.text` | body | `string` | no |
