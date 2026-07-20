# Encodian: Word Extract Text

Extracts text from a Word document in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-extract-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-extract-text?connectionId=$CONNECTION_ID&fileContent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-extract-text?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContent` | string | yes | The file content of the source Microsoft Word file. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `startPage` | number | no | Sets the page number to begin text extraction from. |
| `endPage` | number | no | Sets the page number to end text extraction from. |
| `removeComments` | boolean | no | Set whether comments should be removed prior to extracting text. |
| `acceptChanges` | boolean | no | Set whether tracked changes should be accepted prior to extracting text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "httpStatusCode": 1,
      "httpStatusMessage": "string",
      "operationId": "string",
      "operationStatus": "string",
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `httpStatusCode` | number |  |
| `httpStatusMessage` | string |  |
| `operationId` | string |  |
| `operationStatus` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Word/GetTextFromWord` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/word-extract-text.md) for the provider-specific parameters and requirements.

