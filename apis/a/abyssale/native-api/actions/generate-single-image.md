# Generate Single Image with Abyssale

Generates a single image in Abyssale.

## Endpoint

- **Method:** `POST`
- **Path:** `/banner-builder/:designId/generate`
- **Base URL:** `https://api.abyssale.com`
- **Official documentation:** [Generate Single Image](https://developers.abyssale.com/rest-api/generation/synchronous-generation/generate-single-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `designId` | path | `string` | yes | Design ID to generate from |
| `elements` | body | `object` | yes | Customization payload for design elements |
| `template_format_name` | body | `string` | yes | Format name to generate |
