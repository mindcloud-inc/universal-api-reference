# Remove Property Image with Wasi

Deletes a property image from Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/property/remove-image/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Remove Property Image](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_image` | query | `number` | yes | Image ID to remove. |
| `id_property` | path | `number` | yes | Wasi property ID. |
