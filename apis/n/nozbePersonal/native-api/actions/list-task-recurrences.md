# List Task Recurrences with Nozbe Personal

Retrieves accessible task recurrences from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/task_recurrences`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Task Recurrences](https://api4.nozbe.com/v1/api#/task_recurrences/getTaskRecurrences)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | query | `string` | no |
| `current_task_id` | query | `string` | no |
| `fields` | query | `string` | no |
| `sortBy` | query | `string` | no |
