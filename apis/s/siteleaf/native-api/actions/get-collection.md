# Get Collection with Siteleaf

Retrieves a collection from Siteleaf.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/collections/:path`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Get Collection](https://learn.siteleaf.com/api/collections/#get-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
