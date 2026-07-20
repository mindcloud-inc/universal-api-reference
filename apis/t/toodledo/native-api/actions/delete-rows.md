# Delete Rows with Toodledo

Deletes existing rows from Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/rows/delete.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Delete Rows](https://api.toodledo.com/3/rows/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rows` | body | `string` | yes | JSON-encoded array of row delete objects, each containing list and row. |
