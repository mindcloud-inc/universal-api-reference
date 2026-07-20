# Delete Links in Bulk with Short.io

Deletes links in bulk from Short.io.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/links/delete_bulk`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Delete Links in Bulk](https://developers.short.io/reference/delete_links-delete-bulk)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_ids[]` | body | `array<string>` | yes |
