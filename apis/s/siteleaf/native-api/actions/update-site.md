# Update Site with Siteleaf

Updates an existing site in Siteleaf.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sites/:site_id`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Update Site](https://learn.siteleaf.com/api/sites/#update-a-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | no | Siteleaf site identifier |
| `title` | body | `string` | no | Updated site title |
