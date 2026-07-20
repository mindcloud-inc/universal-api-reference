# Delete Outlines with Toodledo

Deletes existing outlines from Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/outlines/delete.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Delete Outlines](https://api.toodledo.com/3/outlines/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outlines` | body | `string` | yes | JSON-encoded array of outline IDs to delete. |
