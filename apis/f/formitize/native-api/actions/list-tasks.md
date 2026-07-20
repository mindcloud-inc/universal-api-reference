# List Tasks with Formitize

Retrieves tasks from Formitize.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/task/`
- **Base URL:** `https://service.formitize.com/api/rest/v2`
- **Official documentation:** [List Tasks](https://mitechnologies.github.io/Formitize-NET-API/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignedTo` | query | `string` | no | Filter by assigned user ID. |
| `clientID` | query | `string` | no | Filter by related client ID. |
| `from` | query | `string` | no | Filter tasks with a due date on or after this date. |
| `order` | query | `string` | no | Sort direction on due date. |
| `search` | query | `string` | no | Search task title and description. |
| `status` | query | `string` | no | Filter by task status. |
| `taskType` | query | `string` | no | Filter by task type. |
| `to` | query | `string` | no | Filter tasks with a due date on or before this date. |
