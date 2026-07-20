# Encodian - Image: Image - Add Text Watermark

Creates an image with a text watermark in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-text-watermark
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-text-watermark" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "text": "string",
  "finalOperation": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-add-text-watermark', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "text": "string",
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
| `fileContent` | string | no | Base64 content of the source image file. |
| `text` | string | yes | The text to embed as a watermark within the image. |
| `watermarkPosition` | list | no | Position of the text watermark within the image. One of: `BottomLeft`, `BottomRight`, `CentreHorizontal`, `CentreVertical`, `Diagonal`, `TopLeft`, `TopRight`. Default: `BottomLeft`. |
| `font` | string | no | Font applied to the text watermark. Default is Arial. |
| `textColour` | string | no | HTML colour for the text watermark. Default is #E81123. |
| `textSize` | number | no | Font size for the text watermark. Default is 10. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `finalOperation` | boolean | yes | Return the processed file content instead of only an operation ID. Default: `true`. |
| `operationId` | string | no | Advanced: use a previous Encodian operation ID instead of file content. |

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

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/AddTextWatermarkToImage` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-add-text-watermark.md) for the provider-specific parameters and requirements.

