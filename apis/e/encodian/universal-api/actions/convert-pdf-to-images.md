# Encodian: Convert PDF To Images

Converts a PDF document to images in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-images" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "imageFormat": "PNG"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-pdf-to-images', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "imageFormat": "PNG"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | A Base64 encoded representation of the PDF file to be processed. |
| `imageFormat` | string | yes | Set the format for the output image files. Default: `PNG`. |
| `filenamePrefix` | string | no | The prefix filename for the output image files. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resolution` | number | no | Set the output image resolution. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "documents": [
        {}
      ],
      "Errors": [
        "string"
      ],
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
| `documents` | array<object> | The collection of images created from the PDF document. |
| `Errors` | array<string> | Any error messages returned by the operation. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Indicates whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/ConvertPdfToImages` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-pdf-to-images.md) for the provider-specific parameters and requirements.

