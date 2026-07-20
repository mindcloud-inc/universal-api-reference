# Update Collection with Siteleaf

Updates an existing collection in Siteleaf.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id/collections/:path`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Update Collection](https://learn.siteleaf.com/api/collections/#update-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
| `title` | body | `string` | no | Updated collection title |
