# Rename File with Dynalist

Renames a file or folder in Dynalist.

## Endpoint

- **Method:** `POST`
- **Path:** `/file/edit`
- **Base URL:** `https://dynalist.io/api/v1/`
- **Official documentation:** [Rename File](https://apidocs.dynalist.io/#make-changes-to-documents-and-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `changes[0].type` | body | `string` | yes | Type of file to rename: document or folder. |
| `changes[0].file_id` | body | `string` | yes | ID of the document or folder to rename. |
| `changes[0].title` | body | `string` | yes | New title. |
