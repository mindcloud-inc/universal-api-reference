# Update Rows with Toodledo

Updates existing rows in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/rows/edit.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Update Rows](https://api.toodledo.com/3/rows/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rows` | body | `string` | yes | JSON-encoded array of up to 50 row objects. Each row must include id and cells. |
