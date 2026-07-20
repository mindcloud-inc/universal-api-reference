# Create Notes with Toodledo

Creates notes in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes/add.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Create Notes](https://api.toodledo.com/3/notes/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notes` | body | `string` | yes | JSON-encoded array of up to 50 note objects using title, folder, private, added, text, and optional ref. |
