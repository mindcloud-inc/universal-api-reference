# Create Task with Streak

Creates a new task in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/boxes/:boxKey/tasks`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Create Task](https://streak.readme.io/reference/create-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boxKey` | path | `string` | yes |
| `text` | body | `string` | yes |
| `dueDate` | body | `date` | no |
| `assignedToSharingEntries[].email` | body | `string` | no |
