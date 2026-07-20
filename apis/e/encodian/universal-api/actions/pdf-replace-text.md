# Encodian: PDF Replace Text

Replaces text in a PDF with Encodian.

```
PUT https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-replace-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-replace-text" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "fileContent": "string",
  "phrases[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/pdf-replace-text', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "fileContent": "string",
    "phrases[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | The filename of the source PDF document including the file extension. |
| `fileContent` | string | yes | A Base64 encoded representation of the source PDF document. |
| `phrases[]` | array<object> | yes | An array of phrases containing the search and replacement instructions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnFile` | boolean | no | Set whether to return the file or just an operation ID. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "fileContent": "string",
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> | Errors returned by Encodian, if any. |
| `fileContent` | string | The Base64 encoded updated PDF file. |
| `httpStatusCode` | number | The HTTP status code returned by Encodian. |
| `httpStatusMessage` | string | The HTTP status message returned by Encodian. |
| `operationId` | string | The Encodian operation ID. |
| `operationStatus` | string | The Encodian operation status. |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/PDF/PdfSearchAndReplaceText` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pdf-replace-text.md) for the provider-specific parameters and requirements.

