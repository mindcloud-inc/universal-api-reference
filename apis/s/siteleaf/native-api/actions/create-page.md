# Create Page with Siteleaf

Creates a new page in Siteleaf.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/pages`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Create Page](https://learn.siteleaf.com/api/pages/#create-a-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | no | Siteleaf site identifier |
| `title` | body | `string` | no | Page title |
