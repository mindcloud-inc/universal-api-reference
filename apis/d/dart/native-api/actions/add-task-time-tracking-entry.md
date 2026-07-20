# Add Task Time Tracking Entry with Dart

Adds a time tracking entry to a Dart task.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/:id/time-tracking`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [Add Task Time Tracking Entry](https://app.dartai.com/api/v0/public/docs/#/Task/addTaskTimeTracking)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customPropertyName` | body | `string` | no |
| `finishedAt` | body | `string` | no |
| `id` | path | `string` | no |
| `startedAt` | body | `string` | no |
| `user` | body | `string` | no |
