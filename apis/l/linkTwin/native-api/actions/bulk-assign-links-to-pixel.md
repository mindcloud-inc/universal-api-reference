# Bulk Assign Links To Pixel with LinkTwin

Adds or removes multiple links for a pixel in LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/pixel/:id/links`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Bulk Assign Links To Pixel](https://linktw.in/developers#bulk-assign-links-to-pixel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `add` | body | `object` | no |
| `remove` | body | `object` | no |
