# Uncomplete Node with Workflowy

Marks a Workflowy node as not completed.

## Endpoint

- **Method:** `POST`
- **Path:** `/nodes/:id/uncomplete`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Uncomplete Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the node to uncomplete. |
