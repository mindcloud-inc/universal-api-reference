# <img src="https://images.mindcloud.co/apps/icons/images-1_1777381282252.png" alt="Tinify logo" width="28" height="28"> Tinify: Universal API

Compress, convert, resize, preserve metadata, and store optimized AVIF, WebP, JPEG, and PNG images with the Tinify API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tinify/latest
- **Category:** Content & Files / Storage
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tinify.com
- **Vendor API docs:** https://tinify.com/developers/reference/http

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Optimized Image](actions/download-optimized-image.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinify/latest/actions/download-optimized-image?connectionId=$CONNECTION_ID&outputId=zr1jp6xybr82ge0s683x67rgwsawjw4z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Compress Image From File](actions/compress-image-from-file.md) | POST | Compresses an uploaded image file in Tinify. |
| [Compress Image From URL](actions/compress-image-from-url.md) | POST | Compresses an image from a URL in Tinify. |
| [Convert Image](actions/convert-image.md) | PUT | Converts an optimized image in Tinify. |
| [Convert Image With Background](actions/convert-image-with-background.md) | PUT | Converts an optimized image and fills its background in Tinify. |
| [Download Optimized Image](actions/download-optimized-image.md) | GET | Downloads an optimized image from Tinify. |
| [Preserve Metadata](actions/preserve-metadata.md) | PUT | Preserves metadata in an optimized image in Tinify. |
| [Resize Image](actions/resize-image.md) | PUT | Resizes an optimized image in Tinify. |
| [Store Image To Amazon S3](actions/store-image-to-amazon-s3.md) | POST | Stores an optimized image from Tinify in Amazon S3. |
| [Store Image To Google Cloud Storage](actions/store-image-to-google-cloud-storage.md) | POST | Stores an optimized image from Tinify in Google Cloud Storage. |

