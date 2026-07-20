# Generate GIF Memix with Memix

Retrieves a generated GIF from Memix.

## Endpoint

- **Method:** `GET`
- **Path:** `/memix-:template_slug.gif`
- **Base URL:** `https://api.memix.com`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_slug` | path | `string` | yes | Memix template slug. |
| `text` | query | `string` | no | Text rendered into the generated Memix when the template supports it. |
| `image_url` | query | `string` | no | Source image URL used when the template supports image input. |
| `image_id` | query | `string` | no | Memix image identifier used when the template supports image input. |
| `watermark_align` | query | `list` | no | Optional watermark alignment for the generated Memix. Accepted values: `0`, `1`. |
| `duration` | query | `number` | no | Optional output duration in seconds when supported. |
