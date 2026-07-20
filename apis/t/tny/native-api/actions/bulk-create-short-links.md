# Bulk Create Short Links with Tny

Creates multiple shortened links in Tny.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/shorten/bulk`
- **Base URL:** `https://www.tny.dev`
- **Official documentation:** [Bulk Create Short Links](https://www.tny.dev/api-docs#bulk-shorten)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `links` | body | `list<object>` | yes | Array of link objects to create. Each item requires url and can include customSlug and domain_id. |
