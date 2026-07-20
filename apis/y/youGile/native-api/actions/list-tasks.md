# List tasks with YouGile

Retrieves a list of tasks from YouGile.

## Endpoint

- **Method:** `GET`
- **Path:** `/task-list`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List tasks](https://ru.yougile.com/api-v2#/operations/TaskController_search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted tasks in the results. |
| `title` | query | `string` | no | Filter tasks by title. |
| `columnId` | query | `string` | no | Filter tasks by column ID. |
| `assignedTo` | query | `string` | no | Filter tasks by assignee ID or comma-separated assignee IDs. |
| `stickerId` | query | `string` | no | Filter tasks by sticker ID. |
| `stickerStateId` | query | `string` | no | Filter tasks by sticker state ID. |
