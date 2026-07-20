# Create Rows with Toodledo

Creates rows in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/rows/add.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Create Rows](https://api.toodledo.com/3/rows/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rows` | body | `string` | yes | JSON-encoded array of up to 50 row objects. Each row must include list, cells, and ref. |
