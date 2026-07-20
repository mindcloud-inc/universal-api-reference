# Upload Property Image with Wasi

Uploads a property image to Wasi.

## Endpoint

- **Method:** `POST`
- **Path:** `/property/upload-image/:id_property`
- **Base URL:** `https://api.wasi.co/v1`
- **Official documentation:** [Upload Property Image](https://api.wasi.co/docs/en/guide/properties.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_property` | path | `number` | yes | Wasi property ID. |
| `image` | query | `string` | yes | Image file payload placeholder for Wasi multipart upload scaffolding. |
