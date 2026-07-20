# Move Folder Item with Canva

Moves an item to another Canva folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/folders/move`
- **Base URL:** `https://api.canva.com/rest`
- **Official documentation:** [Move Folder Item](https://www.canva.dev/docs/connect/api-reference/folders/move-folder-item/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `item_id` | body | `string` | yes | Maximum length: 50. |
| `to_folder_id` | body | `string` | yes | Maximum length: 50. |
