# Encodian: PDF Add Page Numbers

Adds page numbers to a PDF in Encodian.

```
PUT https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-add-page-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-add-page-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-add-page-numbers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The PDF filename to be processed, including file extension. |
| `fileContent` | string | yes | A Base64 encoded representation of the PDF document to be processed. |
| `startPage` | number | no | Set which page to start adding page numbers from. |
| `startNumber` | number | no | Set the starting number for the page numbers added to the document. |
| `pageNumberFormat` | string | no | Set the format of the page numbers added to the document. |
| `horizontalAlignment` | string | no | Set the horizontal alignment of the page numbers added to the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnFile` | boolean | no | Sets whether the action should return a file or an operation ID. Default: `true`. |

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
| `FileContent` | string | The Base64 encoded processed PDF document. |
| `Filename` | string | The filename of the processed PDF document. |
| `HttpStatusCode` | number | The HTTP status code for the response. |
| `HttpStatusMessage` | string | The HTTP status message for the response. |
| `OperationId` | string | The unique ID assigned to this operation. |
| `OperationStatus` | string | Whether the operation completed, queued, or failed. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/AddPageNumbers` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-add-page-numbers.md) for the provider-specific parameters and requirements.

