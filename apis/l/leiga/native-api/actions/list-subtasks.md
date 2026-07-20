# List Subtasks with Leiga

Retrieves subtasks from Leiga for an issue.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/list-subtask`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [List Subtasks](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741848.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Parent Issue ID |
