# Encodian - Image: Image - Extract Metadata

Retrieves image metadata from Encodian - Image.

```
GET https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-extract-metadata?${params}`, {
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
| `fileContent` | string | yes | Base64 content of the source image file. |
| `simplifiedLatLongFormat` | boolean | no | Return latitude and longitude as formatted strings when location metadata is available. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bitsPerPixel": 1,
      "Errors": [
        "string"
      ],
      "exifDataJson": "string",
      "fileSize": "string",
      "hasExifData": true,
      "hasXmpData": true,
      "height": 1,
      "horizontalResolution": 1,
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "imageFormat": "string",
      "OperationId": "string",
      "OperationStatus": "string",
      "orientation": "string",
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
| `bitsPerPixel` | number | Bits per pixel. |
| `Errors` | array<string> | Error messages, if any. |
| `exifDataJson` | string | EXIF data as a JSON string. |
| `fileSize` | string | Image file size in MB. |
| `hasExifData` | boolean | Whether EXIF data is present. |
| `hasXmpData` | boolean | Whether XMP data is present. |
| `height` | number | Image height in pixels. |
| `horizontalResolution` | number | Horizontal resolution in DPI. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `imageFormat` | string | Image file format. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |
| `orientation` | string | Image orientation. |
| `verticalResolution` | number | Vertical resolution in DPI. |
| `width` | number | Image width in pixels. |

## Native endpoint

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/GetImageInfo` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-extract-metadata.md) for the provider-specific parameters and requirements.

