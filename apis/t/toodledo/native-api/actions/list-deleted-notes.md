# List Deleted Notes with Toodledo

Retrieves deleted notes from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/notes/deleted.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Deleted Notes](https://api.toodledo.com/3/notes/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Return only notes deleted after this GMT Unix timestamp. |
