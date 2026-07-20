# List Nodes with Workflowy

Retrieves child nodes from Workflowy for a parent.

## Endpoint

- **Method:** `GET`
- **Path:** `/nodes`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [List Nodes](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent_id` | query | `string` | no | Node UUID, target key like home or inbox, or None for top-level nodes. |
