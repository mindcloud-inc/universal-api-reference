# Encodian: Convert Word To PDF Form

Converts Word to a PDF form in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word-to-pdf-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word-to-pdf-form" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFilename": "form-output.pdf",
  "filename": "template.docx",
  "fileContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word-to-pdf-form', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFilename": "form-output.pdf",
    "filename": "template.docx",
    "fileContent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFilename` | string | yes | The filename to assign to the resulting PDF document. Example: `form-output.pdf`. |
| `filename` | string | yes | The filename including extension of the file to be converted. Example: `template.docx`. |
| `fileContent` | string | yes | The base64 encoded representation of the file to be converted. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnFile` | boolean | no | Set whether the action returns a file or an operation ID. Default: `true`. |

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
      "filename": "Ava Chen",
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
| `errors` | array<string> |  |
| `fileContent` | string |  |
| `filename` | string |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Conversion/WordToPdfForm` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-word-to-pdf-form.md) for the provider-specific parameters and requirements.

