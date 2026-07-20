# Update Pixel with LinkTwin

Updates an existing pixel in LinkTwin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pixel/:id/update`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Update Pixel](https://linktw.in/developers#update-pixel)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | no |
| `tag` | body | `string` | yes |
