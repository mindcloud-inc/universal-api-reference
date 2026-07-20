# Move File with Dynalist

Moves a file or folder in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Move File](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `changes[0].type` | body | `string` | yes | Type of file to move: document or folder. |
| `changes[0].file_id` | body | `string` | yes | ID of the document or folder to move. |
| `changes[0].parent_id` | body | `string` | yes | Target parent folder ID. |
| `changes[0].index` | body | `number` | yes | Zero-indexed destination position; use -1 for the end. |
