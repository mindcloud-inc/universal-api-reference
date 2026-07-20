# Delete Lists with Toodledo

Deletes existing lists from Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/delete.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Delete Lists](https://api.toodledo.com/3/lists/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lists` | body | `string` | yes | JSON-encoded array of list IDs to delete. |
