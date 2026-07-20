# List Deleted Outlines with Toodledo

Retrieves deleted outlines from Toodledo.

## Endpoint

- **Method:** `GET`
- **Path:** `/outlines/deleted.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [List Deleted Outlines](https://api.toodledo.com/3/outlines/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `number` | no | Return only outlines deleted after this GMT Unix timestamp. |
