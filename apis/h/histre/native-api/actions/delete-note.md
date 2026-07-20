# Delete a Note with Histre

Deletes a note from Histre.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/note/`
- **Base URL:** `https://histre.com`
- **Official documentation:** [Delete a Note](https://histre.com/features/api/notes/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | URL whose Histre note should be deleted. This is the recommended identifier when deleting a note created from a page URL. |
| `note_id` | body | `string` | no | UUID of the Histre note to delete. This is not the item_id returned by the note create endpoint. |
