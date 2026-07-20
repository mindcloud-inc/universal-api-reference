# Create Lists with Toodledo

Creates lists in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists/add.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Create Lists](https://api.toodledo.com/3/lists/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lists` | body | `string` | yes | JSON-encoded array of up to 50 list objects. Each list must include title and ref. |
