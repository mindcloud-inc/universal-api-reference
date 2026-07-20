# Reorder Subtasks with Kanban Tool

## Endpoint

- **Method:** `PUT`
- **Path:** `/subtasks/reorder.json`
- **Base URL:** `https://{domain}.kanbantool.com/api/v3`
- **Official documentation:** [Reorder Subtasks](https://kanbantool.com/developer/api-v3#reordering-subtasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `task_id` | body | `number` | yes | Parent task ID whose subtasks should be reordered. |
| `ids` | body | `object` | yes | JSON array of subtask IDs in the desired final order. |
