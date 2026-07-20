# List Tasks with Attio

Retrieves tasks from Attio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/tasks`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [List Tasks](https://docs.attio.com/rest-api/endpoint-reference/tasks/list-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linked_object` | query | `string` | no | Filter tasks to those linked to a record from the specified object. |
| `linked_record_id` | query | `string` | no | Filter tasks to those linked to the specified record ID. |
| `assignee` | query | `string` | no | Filter tasks by assignee. |
| `is_completed` | query | `boolean` | no | Filter tasks by whether they are completed. |
| `sort` | query | `list<string>` | no | Sort order for the returned tasks. Accepted values: `created_at:asc`, `created_at:desc`. |
