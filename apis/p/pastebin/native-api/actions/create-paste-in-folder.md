# Create Paste In Folder with Pastebin

Creates a paste in a Pastebin folder.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_post.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Create Paste In Folder](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_paste_code` | body | `string` | yes | The text content to include in the folder paste. |
| `api_folder_key` | body | `string` | yes | Existing Pastebin folder key for the destination folder. |
