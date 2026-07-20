# Create Outlines with Toodledo

Creates outlines in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/outlines/add.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Create Outlines](https://api.toodledo.com/3/outlines/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outlines` | body | `string` | yes | JSON-encoded array of up to 50 outline objects. Each outline must include title and ref. |
