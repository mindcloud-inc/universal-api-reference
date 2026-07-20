# Move Documents Between Folders with Docsumo

Moves documents between folders in Docsumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/eevee/apikey/move/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Move Documents Between Folders](https://support.docsumo.com/reference/move-documents-between-folders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dest_folder_id` | body | `string` | yes | Folder ID to move documents to. Use an empty string for My Documents. |
| `doc_ids[]` | body | `array<string>` | yes | One or more document IDs to move. |
| `source_folder_id` | body | `string` | yes | Folder ID to move documents from. Use an empty string for My Documents. |
