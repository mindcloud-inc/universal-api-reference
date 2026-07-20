# Insert Node with Dynalist

Creates a new document node in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/doc/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Insert Node](https://apidocs.dynalist.io/#make-change-to-the-content-of-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | body | `string` | yes | ID of the document to edit. |
| `changes[0].parent_id` | body | `string` | yes | ID of the parent node. |
| `changes[0].index` | body | `number` | yes | Zero-indexed destination position; use -1 for the end. |
| `changes[0].content` | body | `string` | yes | Node content. |
| `changes[0].note` | body | `string` | no | Optional node note. |
| `changes[0].checked` | body | `boolean` | no | Whether the node is checked. |
| `changes[0].checkbox` | body | `boolean` | no | Whether the node has a checkbox. |
| `changes[0].heading` | body | `number` | no | Heading level. |
| `changes[0].color` | body | `number` | no | Dynalist color index. |
