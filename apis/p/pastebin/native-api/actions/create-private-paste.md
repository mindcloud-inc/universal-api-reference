# Create Private Paste with Pastebin

Creates a private paste in Pastebin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_post.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Create Private Paste](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_paste_code` | body | `string` | yes | The text content to include in the private Pastebin paste. |
