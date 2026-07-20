# <img src="https://images.mindcloud.co/apps/icons/changephotos_1776869613814.png" alt="change.photos logo" width="28" height="28"> change.photos: Universal API

change.photos is an API for transforming images at scale, including resizing, conversion, compression, rotation, flipping, grayscale, blur, sharpening, quality adjustment, and tint operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/changephotos/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.change.photos
- **Vendor API docs:** https://www.change.photos/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Adjust Image Quality](actions/adjust-image-quality.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/changephotos/latest/actions/adjust-image-quality" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com/photo.jpg",
  "quality": "80"
}'
```

## Actions (12)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Adjust Image Quality](actions/adjust-image-quality.md) | POST | Creates an image with adjusted quality in change.photos. |
| [Blur Image](actions/blur-image.md) | POST | Creates a blurred image in change.photos. |
| [Compress Image](actions/compress-image.md) | POST | Creates a compressed image in change.photos. |
| [Convert Image Format](actions/convert-image-format.md) | POST | Creates an image in a new format in change.photos. |
| [Flip Image Horizontally](actions/flip-image-horizontally.md) | POST | Creates a horizontally flipped image in change.photos. |
| [Flip Image Vertically](actions/flip-image-vertically.md) | POST | Creates a vertically flipped image in change.photos. |
| [Grayscale Image](actions/grayscale-image.md) | POST | Creates a grayscale image in change.photos. |
| [Resize Image](actions/resize-image.md) | POST | Creates a resized image in change.photos. |
| [Rotate Image](actions/rotate-image.md) | POST | Creates a rotated image in change.photos. |
| [Sharpen Image](actions/sharpen-image.md) | POST | Creates a sharpened image in change.photos. |
| [Tint Image](actions/tint-image.md) | POST | Creates a tinted image in change.photos. |
| [Transform Image](actions/transform-image.md) | POST | Creates a transformed image in change.photos. |

