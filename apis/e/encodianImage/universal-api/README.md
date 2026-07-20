# <img src="https://images.mindcloud.co/apps/icons/encodian_1777477458627.jpeg" alt="Encodian - Image logo" width="28" height="28"> Encodian - Image: Universal API

Manipulate, transform, optimize, watermark, inspect, and extract text from images using Encodian Flowr Image actions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/encodianImage/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.encodian.com/product/flowr/
- **Vendor API docs:** https://learn.microsoft.com/en-gb/connectors/encodianimage/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Image - Extract Metadata](actions/image-extract-metadata.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Image - Add Image Watermark](actions/image-add-image-watermark.md) | POST | Creates an image with an image watermark in Encodian - Image. |
| [Image - Add Text Watermark](actions/image-add-text-watermark.md) | POST | Creates an image with a text watermark in Encodian - Image. |
| [Image - Clean Up Document](actions/image-clean-up-document.md) | POST | Creates a cleaned-up document image in Encodian - Image. |
| [Image - Clean Up Photo](actions/image-clean-up-photo.md) | POST | Creates a cleaned-up photo image in Encodian - Image. |
| [Image - Compress](actions/image-compress.md) | POST | Creates a compressed image in Encodian - Image. |
| [Image - Convert Format](actions/image-convert-format.md) | POST | Creates an image in a new format in Encodian - Image. |
| [Image - Convert to Grayscale](actions/image-convert-to-grayscale.md) | POST | Creates a grayscale image in Encodian - Image. |
| [Image - Crop](actions/image-crop.md) | POST | Creates a cropped image in Encodian - Image. |
| [Image - Extract Metadata](actions/image-extract-metadata.md) | GET | Retrieves image metadata from Encodian - Image. |
| [Image - Extract Text](actions/image-extract-text.md) | GET | Retrieves text from an image in Encodian - Image. |
| [Image - Flip](actions/image-flip.md) | POST | Creates a flipped image in Encodian - Image. |
| [Image - Remove EXIF Tags](actions/image-remove-exif-tags.md) | POST | Creates an image without EXIF tags in Encodian - Image. |
| [Image - Resize](actions/image-resize.md) | POST | Creates a resized image in Encodian - Image. |
| [Image - Rotate](actions/image-rotate.md) | POST | Creates a rotated image in Encodian - Image. |
| [Image - Rotate by EXIF Data](actions/image-rotate-by-exif-data.md) | POST | Creates a JPG rotated by EXIF data in Encodian - Image. |

