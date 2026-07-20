# Get Files with Siteleaf

Retrieves files or directory contents from Siteleaf.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/source/:name`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Get Files](https://learn.siteleaf.com/api/source/#get-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | no | Source file name or path |
| `site_id` | path | `string` | no | Siteleaf site identifier |
