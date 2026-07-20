# List Deleted Rows with Toodledo

Retrieves deleted rows from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/rows/deleted.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Deleted Rows](https://api.toodledo.com/3/rows/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | query | `string` | yes | Hexadecimal list ID whose deleted rows should be fetched. |
| `after` | query | `number` | no | Return only rows deleted after this GMT Unix timestamp. |
