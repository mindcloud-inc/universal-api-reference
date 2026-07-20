# Preview JPEG Memix with Memix

Retrieves a JPEG preview from Memix.

## Endpoint

- **Method:** `GET`
- **Path:** `/preview/memix-:template_slug.jpeg`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_slug` | path | `string` | yes | Memix template slug. |
| `text` | query | `string` | no | Text rendered into the preview when the template supports it. |
| `image_url` | query | `string` | no | Source image URL used when the template supports image input. |
| `image_id` | query | `string` | no | Memix image identifier used when the template supports image input. |
