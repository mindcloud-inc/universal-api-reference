# List Tasks with WebWork Time Tracker

Retrieves project tasks from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Tasks](https://api-docs.webwork-tracker.com/api/tasks/gettasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `project_id` | query | `number` | no |
| `contract_id` | query | `number` | no |
| `status` | query | `number` | no |
| `priority` | query | `number` | no |
| `parent_id` | query | `string` | no |
| `order_by` | query | `string` | no |
