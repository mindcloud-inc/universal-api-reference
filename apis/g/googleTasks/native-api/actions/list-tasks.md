# List Tasks with Google Tasks

Finds tasks in a Google Tasks list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:tasklist/tasks`
- **Base URL:** `https://tasks.googleapis.com/tasks/v1`
- **Official documentation:** [List Tasks](https://developers.google.com/workspace/tasks/reference/rest/v1/tasks/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tasklist` | path | `list` | yes |
| `completedMin` | query | `date` | no |
| `completedMax` | query | `date` | no |
| `dueMin` | query | `date` | no |
| `dueMax` | query | `date` | no |
| `updatedMin` | query | `date` | no |
| `showCompleted` | query | `boolean` | no |
| `showDeleted` | query | `boolean` | no |
| `showHidden` | query | `boolean` | no |
