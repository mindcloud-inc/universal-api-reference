# Encodian: PowerPoint Compress

Compresses a PowerPoint file in Encodian.

```
PUT https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-compress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-compress" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileName": "Ava Chen",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/power-point-compress', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileName": "Ava Chen",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileName` | string | yes | The filename of the source file; include the .pptx extension. |
| `fileContent` | string | yes | The Base64 encoded content of the source PowerPoint file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `compressionRate` | list | no | Sets the image compression rate; higher values generate smaller files. One of: `0`, `1`, `2`, `3`. Default: `Low`. |
| `compressEmbeddedFonts` | boolean | no | Remove unused characters from embedded fonts. |
| `removeUnusedLayoutSlides` | boolean | no | Remove unused layout slides from the presentation. |
| `removeUnusedMasterSlides` | boolean | no | Remove unused master slides from the presentation. |
| `resizeImagesToFrameSize` | boolean | no | Resize images to fit their displayed frames. |
| `cultureName` | string | no | Culture name used when processing the request. |

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
| `Errors` | array<string> | Errors returned by Encodian, if any. |
| `FileContent` | string | The Base64 encoded processed presentation file. |
| `Filename` | string | The filename of the processed file. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PowerPoint/CompressPowerPoint` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/power-point-compress.md) for the provider-specific parameters and requirements.

