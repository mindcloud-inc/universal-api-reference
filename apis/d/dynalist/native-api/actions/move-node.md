# Move Node with Dynalist

Moves a document node in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Move Node](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | ID of the document to edit. |
| `changes[0].node_id` | body | `string` | yes | ID of the node to move. |
| `changes[0].parent_id` | body | `string` | yes | Target parent node ID. |
| `changes[0].index` | body | `number` | yes | Zero-indexed destination position; use -1 for the end. |
