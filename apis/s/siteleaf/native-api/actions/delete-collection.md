# Delete Collection with Siteleaf

Deletes an existing collection from Siteleaf.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sites/:site_id/collections/:path`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Delete Collection](https://learn.siteleaf.com/api/collections/#delete-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
