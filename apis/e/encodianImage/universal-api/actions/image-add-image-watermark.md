# Encodian - Image: Image - Add Image Watermark

Creates an image with an image watermark in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-image-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-image-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "fileContent": "string",
  "watermarkFilename": "Ava Chen",
  "watermarkFileContent": "string",
  "watermarkPosition": "CentreHorizontal"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-image-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "fileContent": "string",
    "watermarkFilename": "Ava Chen",
    "watermarkFileContent": "string",
    "watermarkPosition": "CentreHorizontal"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The filename of the source file. The file extension is mandatory, such as file.png. |
| `fileContent` | string | yes | Base64 content of the source image file. |
| `watermarkFilename` | string | yes | The filename of the watermark image file. The file extension is mandatory. |
| `watermarkFileContent` | string | yes | Base64 content of the watermark image file. |
| `watermarkPosition` | list | yes | The position of the image watermark on the source image. One of: `BottomLeft`, `BottomRight`, `CentreHorizontal`, `CentreVertical`, `Custom`, `Diagonal`, `TopLeft`, `TopRight`. Default: `CentreHorizontal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageYOffSet` | number | no | Vertical watermark offset in pixels when Watermark Position is Custom. |
| `imageXOffset` | number | no | Horizontal watermark offset in pixels when Watermark Position is Custom. |
| `rotationAngle` | number | no | Rotation angle for the watermark image in degrees. |
| `opacity` | number | no | Watermark opacity from 0.0 to 1.0. Default is 0.7. Default: `0.7`. |
| `alignImage` | boolean | no | Align the source image using EXIF orientation tags. |
| `alignWatermark` | boolean | no | Align the watermark image using EXIF orientation tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Errors": [
        "string"
      ],
      "FileContent": "string",
      "Filename": "Ava Chen",
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Errors` | array<string> | Error messages, if any. |
| `FileContent` | string | Base64 content of the processed image. |
| `Filename` | string | The filename of the processed image. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/AddImageWatermarkToImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-add-image-watermark.md) for the provider-specific parameters and requirements.

