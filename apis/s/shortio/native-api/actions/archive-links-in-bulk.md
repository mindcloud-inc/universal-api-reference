# Archive Links in Bulk with Short.io

Archives links in bulk in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/archive_bulk`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Archive Links in Bulk](https://developers.short.io/reference/post_links-archive-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_ids[]` | body | `array<string>` | yes |
| `domain_id` | body | `string` | no |
