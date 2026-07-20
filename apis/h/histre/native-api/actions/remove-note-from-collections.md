# Remove Note from Collections with Histre

Removes a note from collections in Histre.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections/remove_note/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Remove Note from Collections](https://histre.com/features/api/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url_item_item_id` | body | `string` | yes | Histre URL item ID to remove from the selected collections. |
| `book_ids[]` | body | `array<string>` | yes | One or more Histre collection IDs from which the note will be removed. |
