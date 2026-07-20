# Update Subtask Status with Leiga

Updates a subtask status in Leiga.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/issue/update-subtask-status`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Update Subtask Status](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741846.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | no | Subtask ID |
| `projectId` | body | `number` | no | Project ID |
| `done` | body | `boolean` | no | Done Flag |
