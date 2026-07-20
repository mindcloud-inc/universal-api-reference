# Update Pixel with Recut URL Shortener

Updates an existing tracking pixel in Recut URL Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pixel/:id/update`
- **Base URL:** `https://app.recut.in/api`
- **Official documentation:** [Update Pixel](https://app.recut.in/developers#update-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Pixel ID |
| `name` | body | `string` | no | Pixel name |
| `tag` | body | `string` | yes | Pixel tag |
