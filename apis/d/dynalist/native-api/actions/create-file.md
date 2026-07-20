# Create File with Dynalist

Creates a new file or folder in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Create File](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `changes[0].type` | body | `string` | yes | Type of file to create: document or folder. |
| `changes[0].parent_id` | body | `string` | yes | ID of the parent folder. |
| `changes[0].index` | body | `number` | yes | Zero-indexed destination position; use -1 for the end. |
| `changes[0].title` | body | `string` | no | Optional title for the new file. |
