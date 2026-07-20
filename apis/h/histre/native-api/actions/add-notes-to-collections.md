# Add Notes to Collections with Histre

Adds notes to collections in Histre.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/collections/add_notes/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Add Notes to Collections](https://histre.com/features/api/collections/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url_item_item_ids[]` | body | `array<string>` | yes | One or more Histre URL item IDs to add to collections. |
| `book_ids[]` | body | `array<string>` | yes | One or more Histre collection IDs that should receive the notes. |
