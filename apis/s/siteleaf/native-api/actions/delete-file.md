# Delete File with Siteleaf

Deletes an existing file from Siteleaf.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:site_id/source/:name`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Delete File](https://learn.siteleaf.com/api/source/#delete-a-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | no | Source file name or path |
| `site_id` | path | `string` | no | Siteleaf site identifier |
