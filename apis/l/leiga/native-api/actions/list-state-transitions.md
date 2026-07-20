# List State Transitions with Leiga

Retrieves available state transitions from Leiga.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflow/list/next-state`
- **Base URL:** `https://app.leiga.com/openapi/api`
- **Official documentation:** [List State Transitions](https://share.apidog.com/5a741107-c211-410f-880c-048d1917c984/api-3741858.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `defId` | body | `number` | yes | Workflow ID |
| `stateId` | body | `number` | yes | State ID |
