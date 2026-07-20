# Update Task with Streak

Updates an existing task in Streak.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tasks/:taskKey`
- **Base URL:** `https://api.streak.com`
- **Official documentation:** [Update Task](https://streak.readme.io/reference/update-a-task)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `taskKey` | path | `string` | yes |
| `text` | body | `string` | no |
| `dueDate` | body | `date` | no |
| `status` | body | `string` | no |
| `assignedToSharingEntries[].email` | body | `string` | no |
