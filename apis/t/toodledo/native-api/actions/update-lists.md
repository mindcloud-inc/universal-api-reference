# Update Lists with Toodledo

Updates existing lists in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/edit.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Update Lists](https://api.toodledo.com/3/lists/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lists` | body | `string` | yes | JSON-encoded array of up to 50 list objects. Each list must include id and version. |
