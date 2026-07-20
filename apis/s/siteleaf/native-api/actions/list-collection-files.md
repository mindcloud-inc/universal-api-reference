# List Collection Files with Siteleaf

Retrieves collection files from Siteleaf.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/collections/:path/files`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [List Collection Files](https://learn.siteleaf.com/api/collections/#list-collection-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
