# Create Guest Paste with Pastebin

Creates a guest paste in Pastebin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_post.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Create Guest Paste](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_paste_code` | body | `string` | yes | The text content to include in the Pastebin paste. |
