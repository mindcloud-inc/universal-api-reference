# Reassign Task with Toodledo

Reassigns a task to a collaborator in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/reassign.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Reassign Task](https://api.toodledo.com/3/tasks/doc_collab.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Numeric Toodledo task ID to reassign. |
| `assign` | body | `string` | yes | Collaborator user ID that should receive the reassigned task. |
