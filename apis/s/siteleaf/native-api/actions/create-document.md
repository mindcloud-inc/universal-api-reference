# Create Document with Siteleaf

Creates a new document in Siteleaf.

## Endpoint

- **Method:** `POST`
- **Path:** `/sites/:site_id/collections/:path/documents`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [Create Document](https://learn.siteleaf.com/api/documents/#create-a-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
| `title` | body | `string` | no | Document title |
