# List Time Entries with ProProfs Project

Retrieves a list of time entries from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/time_entries`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Time Entries](https://help.proprofsproject.com/time-entries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Filter time entries by client. |
| `limit` | query | `string` | no | Limit the number of returned time entries. |
| `offset` | query | `string` | no | Offset for returned time entries. |
| `project_id` | query | `string` | no | Filter time entries by project ID. |
| `subtask_id` | query | `string` | no | Filter time entries by subtask ID. |
| `task_id` | query | `string` | no | Filter time entries by task ID. |
| `user_id` | query | `string` | no | Filter time entries by user ID. |
