# List recent tasks with YouGile

Retrieves recent tasks from YouGile in reverse order.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [List recent tasks](https://ru.yougile.com/api-v2#/operations/TaskController_searchReversed)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeDeleted` | query | `boolean` | no | Include deleted tasks in the result. |
| `title` | query | `string` | no | Filter tasks by title. |
| `columnId` | query | `string` | no | Filter tasks by column ID. |
| `assignedTo` | query | `string` | no | Filter tasks by assignee user ID. |
| `stickerId` | query | `string` | no | Filter tasks by sticker ID. |
| `stickerStateId` | query | `string` | no | Filter tasks by sticker state ID. |
