# Get multiple tasks with Asana

Retrieves tasks from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tasks`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get multiple tasks](https://developers.asana.com/reference/gettasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignee` | query | `string` | no |
| `completed_since` | query | `date` | no |
| `limit` | query | `number` | no |
| `modified_since` | query | `date` | no |
| `offset` | query | `string` | no |
| `opt_fields[]` | query | `array<string>` | no |
| `project` | query | `string` | no |
| `section` | query | `string` | no |
| `workspace` | query | `string` | no |
