# List Tasks with ProProfs Project

Retrieves a list of tasks from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Tasks](https://help.proprofsproject.com/tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of records to return. |
| `offset` | query | `string` | no | Start position for fetching records. |
| `project_id` | query | `string` | no | Filter tasks by project ID. |
