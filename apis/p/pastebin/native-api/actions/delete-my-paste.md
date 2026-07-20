# Delete My Paste with Pastebin

Deletes a paste created by the current Pastebin user.

## Endpoint

- **Method:** `POST`
- **Path:** `/api_post.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Delete My Paste](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_paste_key` | body | `string` | yes | Pastebin key for the member-owned paste to delete. |
