# Delete Notes with Toodledo

Deletes existing notes from Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes/delete.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Delete Notes](https://api.toodledo.com/3/notes/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notes` | body | `string` | yes | JSON-encoded array of note IDs to delete. |
