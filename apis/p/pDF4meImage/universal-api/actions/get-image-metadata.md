# PDF4me Image: Get Image Metadata

Retrieves metadata for an image in PDF4me Image.

```
GET https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PDF4me Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&docContent=string&docName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docContent": "string",
  "docName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pDF4meImage/latest/actions/get-image-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `docContent` | string | yes | Base64-encoded PNG or JPG image content. |
| `docName` | string | yes | File name for the uploaded image, including the extension. |
| `imageType` | string | no | Optional image type such as PNG or JPG when the provider needs it. Example: `PNG or JPG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bitsperPixel": 1,
      "fileSize": 1,
      "hasExifData": true,
      "hasXmpData": true,
      "height": 1,
      "horizontalResolution": 1,
      "imageFormat": "string",
      "verticalResolution": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bitsperPixel` | number | Bits per pixel. |
| `fileSize` | number | Image size in bytes. |
| `hasExifData` | boolean | Whether EXIF data is present. |
| `hasXmpData` | boolean | Whether XMP data is present. |
| `height` | number | Image height in pixels. |
| `horizontalResolution` | number | Horizontal resolution. |
| `imageFormat` | string | Detected image format. |
| `verticalResolution` | number | Vertical resolution. |
| `width` | number | Image width in pixels. |

## Native endpoint

Through the native PDF4me Image API, this operation is `POST /GetImageMetadata` (base URL `https://api.pdf4me.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-metadata.md) for the provider-specific parameters and requirements.

