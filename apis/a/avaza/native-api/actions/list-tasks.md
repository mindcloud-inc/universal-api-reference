# List Tasks with Avaza

Retrieves tasks from Avaza.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/Task`
- **Base URL:** `https://api.avaza.com`
- **Official documentation:** [List Tasks](https://api.avaza.com/#!/Task/Task_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `UpdatedAfter` | query | `date` | no | Optional filter to records updated after a specific date. |
| `isComplete` | query | `boolean` | no | Optional filter to only display tasks linked to a Task Status where isComplete=false, or where isComplete=true |
| `ProjectID` | query | `number` | no | Optional filter to only display tasks belonging to a specific ProjectID |
| `TaskStatusCode` | query | `string` | no | Optional filter to only display tasks with a specific status |
| `TaskPriorityCode` | query | `string` | no | Optional filter to only display tasks with a specific priority |
| `DueDateFrom` | query | `date` | no | Optional filter to only display tasks with a Due Date after DueDateFrom |
| `DueDateTo` | query | `date` | no | Optional filter to only display tasks with a Due Date before DueDateTo |
| `AssignedToUserIDs` | query | `list<number>` | no | Optional filter to only display tasks with at least one of the provided UserIDs set as the Assigned User. |
