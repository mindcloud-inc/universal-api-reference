# Encodian - Image: Image - Crop

Creates a cropped image in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-crop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-crop" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cropType": "Border",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-crop', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cropType": "Border",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cropType` | list | yes | Crop method to use, such as borders or rectangle. One of: `Border`, `Rectangle`. |
| `fileContent` | string | yes | Base64 content of the source image file. |
| `leftBorder` | number | no | Pixel adjustment for the left border. |
| `rightBorder` | number | no | Pixel adjustment for the right border. |
| `topBorder` | number | no | Pixel adjustment for the top border. |
| `bottomBorder` | number | no | Pixel adjustment for the bottom border. |
| `upperLeftX` | number | no | Upper-left X coordinate of the crop area in pixels. |
| `upperLeftY` | number | no | Upper-left Y coordinate of the crop area in pixels. |
| `width` | number | no | Crop area width in pixels. |
| `height` | number | no | Crop area height in pixels. |

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
| `FileContent` | string | Base64 content of the cropped image. |
| `HttpStatusCode` | number | HTTP status code. |
| `HttpStatusMessage` | string | HTTP status message. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/CropImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-crop.md) for the provider-specific parameters and requirements.

