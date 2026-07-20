# List Tasks with Close

Retrieves tasks from Close.

## Endpoint

- **Method:** `GET`
- **Path:** `/task/`
- **Base URL:** `https://api.close.com/api/v1`
- **Official documentation:** [List Tasks](https://developer.close.com/resources/tasks/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `_type` | query | `string` | no | Filter by task type. |
| `assigned_to` | query | `string` | no | Filter by assigned user ID. |
| `is_complete` | query | `boolean` | no | Filter by completion state. |
| `lead_id` | query | `string` | no | Filter by Lead ID. |
| `view` | query | `string` | no | Task list view preset. |
