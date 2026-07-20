# List Deleted Lists with Toodledo

Retrieves deleted lists from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/deleted.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Deleted Lists](https://api.toodledo.com/3/lists/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Return only lists deleted after this GMT Unix timestamp. |
