# Encodian: Word Populate

Populates a Word document in Encodian.

```
POST https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-populate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-populate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "documentData": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-populate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "documentData": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | The Microsoft Word document (DOCX) to populate. |
| `documentData` | string | yes | The JSON data to populate the document with. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jsonParseMode` | string | no | Sets how JSON simple values are parsed. Default: `Standard`. Example: `Standard`. |
| `allowMissingValues` | boolean | no | Allow missing values within the document data. |
| `removeEmptyParagraphs` | boolean | no | Automatically remove empty paragraphs upon execution. |
| `inlineErrors` | boolean | no | Produce errors within the resultant document instead of returning an HTTP 4xx response. |
| `dateTimeFormats` | string | no | One or more specific formats for parsing DateTime values. Example: `yyyy-MM-dd`. |
| `cultureName` | string | no | Set the culture for the document prior to conversion. Example: `en-GB`. |
| `timeZone` | string | no | Set a specific time zone for date and time processing. Example: `UTC`. |

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

Through the native Encodian API, this operation is `POST /api/v1/Word/PopulateWordDocument` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/word-populate.md) for the provider-specific parameters and requirements.

