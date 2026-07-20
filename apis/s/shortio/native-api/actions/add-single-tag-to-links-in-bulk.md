# Add Single Tag to Links in Bulk with Short.io

Adds a tag to links in bulk in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/bulk`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Add Single Tag to Links in Bulk](https://developers.short.io/reference/post_tags-bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | Tag to append. |
| `link_ids[]` | body | `array<string>` | yes | Array of link IDs. |
