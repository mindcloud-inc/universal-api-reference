# List Documents with Siteleaf

Retrieves documents from Siteleaf.

## Endpoint

- **Method:** `GET`
- **Path:** `/sites/:site_id/collections/:path/documents`
- **Base URL:** `https://api.siteleaf.com/v2`
- **Official documentation:** [List Documents](https://learn.siteleaf.com/api/documents/#list-documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | path | `string` | no | Collection path slug |
| `site_id` | path | `string` | no | Siteleaf site identifier |
