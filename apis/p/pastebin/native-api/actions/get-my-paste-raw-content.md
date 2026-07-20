# Get My Paste Raw Content with Pastebin

Retrieves raw content for one of the user's Pastebin pastes.

## Endpoint

- **Method:** `POST`
- **Path:** `https://pastebin.com/api/api_raw.php`
- **Base URL:** `https://pastebin.com/api`
- **Official documentation:** [Get My Paste Raw Content](https://pastebin.com/doc_api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `api_paste_key` | body | `string` | yes | Pastebin key for the member-owned paste to fetch. |
