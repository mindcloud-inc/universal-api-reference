# List CRM Tasks with MindMe

Retrieves CRM tasks from MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/CRM/GetTasksWithFilter`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [List CRM Tasks](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1CRM~1GetTasksWithFilter/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `parentAccountId` | body | `string` | no |
| `subAccountId` | body | `string` | no |
| `userId` | body | `string` | no |
