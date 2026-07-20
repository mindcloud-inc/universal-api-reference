# List Tasks with Hubflo

Retrieves all task records from Hubflo.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://app.hubflo.com/api/v2`
- **Official documentation:** [List Tasks](https://hubflo.readme.io/reference/get_api-v2-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `overdue` | query | `boolean` | no |
| `project_id` | query | `string` | no |
| `contact_id` | query | `string` | no |
| `assignee_id` | query | `string` | no |
| `creator_type` | query | `string` | no |
| `completed` | query | `boolean` | no |
| `parent_id` | query | `string` | no |
| `clickup_id` | query | `string` | no |
| `monday_id` | query | `string` | no |
| `tag` | query | `string` | no |
