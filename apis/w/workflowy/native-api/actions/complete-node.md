# Complete Node with Workflowy

Marks a Workflowy node as completed.

## Endpoint

- **Method:** `POST`
- **Path:** `/nodes/:id/complete`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Complete Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the node to complete. |
