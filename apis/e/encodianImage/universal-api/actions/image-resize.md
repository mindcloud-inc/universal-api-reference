# Encodian - Image: Image - Resize

Creates a resized image in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-resize
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-resize" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileContent": "string",
  "imageResizeType": "Percentage",
  "finalOperation": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-resize', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileContent": "string",
    "imageResizeType": "Percentage",
    "finalOperation": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | The filename of the source image file. The file extension is mandatory. |
| `fileContent` | string | yes | Base64 content of the source image file. |
| `imageResizeType` | list | yes | Whether the image should be resized by ratio or by specific dimensions. One of: `Percentage`, `Specific`. |
| `resizePercentage` | number | no | Percentage used for ratio-based resize. |
| `imageWidth` | number | no | Target image width in pixels. |
| `imageHeight` | number | no | Target image height in pixels. |
| `maintainAspectRatio` | boolean | no | Automatically calculate height from width when resizing to dimensions. |
| `imageResolution` | number | no | Optional output image resolution. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalOperation` | boolean | yes | Return the processed file content instead of only an operation ID. Default: `true`. |

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

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/ResizeImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-resize.md) for the provider-specific parameters and requirements.

