# Update Pixel with JmpTo

Updates an existing pixel in JmpTo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pixel/:id/update`
- **Base URL:** `https://jmpto.net/api`
- **Official documentation:** [Update Pixel](https://jmpto.net/developers#update-pixel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Pixel ID to update. |
| `name` | body | `string` | no | Custom name for the pixel. |
| `tag` | body | `string` | yes | The tag for the pixel. |
