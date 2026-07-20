# Get board time entries with KanbanFlow

Retrieves board time entries from KanbanFlow for a time period.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-entries`
- **Base URL:** `https://kanbanflow.com/api/v1`
- **Official documentation:** [Get board time entries](https://kanbanflow.com/api-docs/time-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Include time entries that start or end after this UTC timestamp. |
| `to` | query | `string` | no | Include time entries that start or end before this UTC timestamp. |
