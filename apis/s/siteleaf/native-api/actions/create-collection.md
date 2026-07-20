# Create Collection with Siteleaf

Creates a new collection in Siteleaf.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/collections`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Create Collection](https://learn.siteleaf.com/api/collections/#create-a-collection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site_id` | path | `string` | no | Siteleaf site identifier |
| `title` | body | `string` | no | Collection title |
