# Unarchive Links in Bulk with Short.io

Unarchives links in bulk in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/unarchive_bulk`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Unarchive Links in Bulk](https://developers.short.io/reference/post_links-unarchive-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_ids[]` | body | `array<string>` | yes |
| `domain_id` | body | `string` | no |
