# Retrieve Node with Workflowy

Retrieves a Workflowy node by target or ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/nodes/:id`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Retrieve Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the node to retrieve. |
