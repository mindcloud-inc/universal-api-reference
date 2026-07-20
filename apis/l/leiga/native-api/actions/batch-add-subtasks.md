# Batch Add Subtasks with Leiga

Creates multiple new subtasks in Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/issue/batch-add-subtask`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [Batch Add Subtasks](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741847.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `issueId` | body | `number` | yes | Parent Issue ID |
