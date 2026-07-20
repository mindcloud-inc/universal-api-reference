# Create or Replace File with Siteleaf

Creates or replaces a file in Siteleaf.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/source/:name`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Create or Replace File](https://learn.siteleaf.com/api/source/#create-or-replace-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | no | File attachment payload |
| `name` | path | `string` | no | Source file name or path |
| `site_id` | path | `string` | no | Siteleaf site identifier |
