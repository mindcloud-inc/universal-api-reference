# Update Outlines with Toodledo

Updates existing outlines in Toodledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/outlines/edit.php`
- **Base URL:** `https://api.toodledo.com/3`
- **Official documentation:** [Update Outlines](https://api.toodledo.com/3/outlines/index.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outlines` | body | `string` | yes | JSON-encoded array of up to 50 outline objects. Each outline must include id and version. |
