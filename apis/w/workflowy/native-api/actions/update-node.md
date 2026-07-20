# Update Node with Workflowy

Updates an existing node in Workflowy.

## Endpoint

- **Method:** `POST`
- **Path:** `/nodes/:id`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Update Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the node to update. |
| `name` | body | `string` | no | The updated text content of the node. |
| `note` | body | `string` | no | The updated note content of the node. |
| `layoutMode` | body | `string` | no | The updated display mode of the node. |
