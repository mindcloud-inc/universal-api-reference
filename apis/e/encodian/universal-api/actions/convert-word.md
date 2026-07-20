# Encodian: Convert Word

Converts a Word document in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormat": "PDF",
  "filename": "hello.docx",
  "fileContent": "Base64 encoded Word file content"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/convert-word', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormat": "PDF",
    "filename": "hello.docx",
    "fileContent": "Base64 encoded Word file content"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `outputFormat` | string | yes | Default: `PDF`. Example: `PDF`. |
| `filename` | string | yes | Example: `hello.docx`. |
| `fileContent` | string | yes | Example: `Base64 encoded Word file content`. |
| `pageOrientation` | string | no | Example: `Portrait`. |
| `pageSize` | string | no | Example: `A4`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `removeMarkup` | boolean | no |  |
| `showRevisionsInBalloons` | string | no | Example: `None`. |
| `trackedChangesInsertedTextColor` | string | no | Example: `Blue`. |
| `trackedChangesDeletedTextColor` | string | no | Example: `Red`. |
| `trackedChangesMovedToTextColor` | string | no | Example: `Green`. |
| `trackedChangesMovedFromTextColor` | string | no | Example: `Purple`. |
| `trackedChangesCommentsColor` | string | no | Example: `Yellow`. |
| `timeZone` | string | no | Example: `UTC`. |
| `cultureName` | string | no | Example: `en-US`. |
| `htmlVersion` | string | no | Example: `HTML5`. |
| `exportListLabels` | string | no | Example: `Auto`. |
| `generateBookmarks` | boolean | no |  |
| `customProperties` | string | no | Example: `None`. |
| `pdfACompliant` | boolean | no |  |
| `pdfAComplianceLevel` | string | no | Example: `1b`. |
| `convertToPdfForm` | boolean | no |  |
| `enableOpenType` | boolean | no |  |
| `pageIndex` | number | no | Example: `1`. |
| `compression` | string | no | Example: `LZW`. |

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

Through the native Encodian API, this operation is `POST /api/v1/Conversion/ConvertWord` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-word.md) for the provider-specific parameters and requirements.

