# Create Node with Workflowy

Creates a new node in Workflowy.

## Endpoint

- **Method:** `POST`
- **Path:** `/nodes`
- **Base URL:** `https://workflowy.com/api/v1`
- **Official documentation:** [Create Node](https://beta.workflowy.com/api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The text content of the new node. |
| `parent_id` | body | `string` | no | Node UUID, target key like home or inbox, or None for a top-level node. |
| `note` | body | `string` | no | Additional note content for the node. |
| `layoutMode` | body | `string` | no | Display mode like bullets, todo, h1, h2, or h3. |
| `position` | body | `string` | no | Where to place the node: top or bottom. |
