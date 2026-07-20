# List Tasks with Assembly.com

Retrieves tasks from Assembly.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [List Tasks](https://docs.assembly.com/reference/retrieve-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdBy` | query | `string` | no | Filter tasks by the internal user that created the task. |
| `parentTaskId` | query | `string` | no | Filter tasks by parent task ID. |
| `status` | query | `string` | no | Filter tasks by status. One of todo, inProgress, completed. Accepted values: `0`, `1`, `2`. |
| `clientId` | query | `string` | no | Filter tasks by assigned client user ID. |
| `internalUserId` | query | `string` | no | Filter tasks by assigned internal user ID. |
| `companyId` | query | `string` | no | Filter tasks by assigned company ID. |
