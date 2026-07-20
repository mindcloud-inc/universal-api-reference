# List Tasks with Podio

Retrieves a list of tasks from Podio.

## Endpoint

- **Method:** `GET`
- **Path:** `/task/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [List Tasks](https://developers.podio.com/doc/tasks/get-tasks-77949)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app[]` | query | `array<number>` | no | App ids to filter by. |
| `completed` | query | `boolean` | no | True to get completed tasks, false to get active tasks. |
| `completed_by` | query | `string` | no | Auth objects for who completed the task. |
| `completed_on` | query | `string` | no | Date or date range for when the task was completed. |
| `created_by` | query | `string` | no | Auth objects for who created the task. |
| `created_on` | query | `string` | no | Date or date range for when the task was created. |
| `created_via` | query | `number` | no | App id the task was created through. |
| `due_date` | query | `string` | no | Date or date range for the due date. |
| `external_id` | query | `string` | no | External id of the associated app item. |
| `files` | query | `boolean` | no | True to get tasks with files, false otherwise. |
| `grouping` | query | `list<string>` | no | Field to group tasks by. Accepted values: `app`, `created_by`, `due_date`, `org`, `responsible`, `space`. |
| `label` | query | `number` | no | Label id to match. |
| `org[]` | query | `array<number>` | no | Organization ids to filter by. |
| `reassigned` | query | `boolean` | no | True to get reassigned tasks, false otherwise. |
| `reference` | query | `string` | no | Task reference in the form type:id. |
| `responsible` | query | `number` | no | Auth objects or user ids assigned to the task. |
| `space[]` | query | `array<number>` | no | Space ids to filter by. |
| `view` | query | `list` | no | Accepted values: `full`. |
