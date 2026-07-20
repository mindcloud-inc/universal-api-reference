# Delete Node with Dynalist

Deletes a document node from Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Delete Node](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | ID of the document to edit. |
| `changes[0].node_id` | body | `string` | yes | ID of the node to delete. |
