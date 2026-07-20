# Encodian - Image: Image - Remove EXIF Tags

Creates an image without EXIF tags in Encodian - Image.

```
POST https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-remove-exif-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Image `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-remove-exif-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "fileName": "Ava Chen",
  "imageType": "JPG"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodianImage/latest/actions/image-remove-exif-tags', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "fileName": "Ava Chen",
    "imageType": "JPG"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | Base64 content of the source image file. |
| `fileName` | string | yes | The filename of the source image file. |
| `imageType` | list | yes | Source image format. Runtime verification showed this endpoint accepts JPG, JPEG, TIF, or TIFF; PNG is rejected by the provider for EXIF removal. One of: `JPEG`, `JPG`, `TIF`, `TIFF`. Default: `JPG`. |

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

Through the native Encodian - Image API, this operation is `POST /api/v1/Image/ImageRemoveExifTags` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/image-remove-exif-tags.md) for the provider-specific parameters and requirements.

