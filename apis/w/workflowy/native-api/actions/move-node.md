# Move Node with Workflowy

Moves a node to a new parent in Workflowy.

## Endpoint

- **Method:** `POST`
- **Path:** `/nodes/:id/move`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Move Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the node to move. |
| `parent_id` | body | `string` | no | The new parent node identifier or target key. |
| `position` | body | `string` | no | Where to place the moved node: top or bottom. |
