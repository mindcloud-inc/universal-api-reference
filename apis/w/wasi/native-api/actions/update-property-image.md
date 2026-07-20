# Update Property Image with Wasi

Updates a property image in Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/gallery/image/update-data/:id_image`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Update Property Image](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `alt` | query | `string` | no | Image alt text. |
| `id_image` | path | `number` | yes | Wasi image ID. |
| `title` | query | `string` | no | Image title. |
