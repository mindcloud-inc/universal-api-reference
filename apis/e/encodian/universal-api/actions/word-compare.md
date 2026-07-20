# Encodian: Word Compare

Compares Word or PDF documents in Encodian.

```
GET https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-compare
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-compare?connectionId=$CONNECTION_ID&fileContentOne=string&fileContentTwo=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContentOne": "string",
  "fileContentTwo": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodian/latest/actions/word-compare?${params}`, {
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
| `fileContentOne` | string | yes | A Base64 encoded representation of the first file to compare. |
| `fileContentTwo` | string | yes | A Base64 encoded representation of the second file to compare. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `author` | string | no | Set the author name used to denote differences in the output document. |
| `ignoreFormatting` | boolean | no | Specifies whether to ignore document formatting differences. |
| `caseInsensitive` | boolean | no | Specifies whether to compare differences in documents as case insensitive. |
| `ignoreComments` | boolean | no | Specifies whether to compare differences in comments. |
| `ignoreTables` | boolean | no | Specifies whether to compare differences in table data. |
| `ignoreFields` | boolean | no | Specifies whether to compare differences in fields. |
| `ignoreFootnotes` | boolean | no | Specifies whether to compare differences in footnotes and endnotes. |
| `ignoreTextboxes` | boolean | no | Specifies whether to compare differences in text boxes. |
| `ignoreHeadersAndFooters` | boolean | no | Specifies whether to compare differences in headers and footers. |

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
| `Errors` | array<string> |  |
| `FileContent` | string |  |
| `Filename` | string |  |
| `HttpStatusCode` | number |  |
| `HttpStatusMessage` | string |  |
| `OperationId` | string |  |
| `OperationStatus` | string |  |

## Native endpoint

Through the native Encodian API, this operation is `POST /api/v1/Word/CompareWordDocuments` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/word-compare.md) for the provider-specific parameters and requirements.

