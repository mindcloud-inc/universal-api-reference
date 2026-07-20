# Update Notes with Toodledo

Updates existing notes in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/notes/edit.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Update Notes](https://api.toodledo.com/3/notes/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `notes` | body | `string` | yes | JSON-encoded array of up to 50 note objects. Each object must include an id. |
