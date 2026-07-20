# Document AI: Extract Document Tables

Extracts tables from a document using Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-tables?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-tables?${params}`, {
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
| `InputFile` | file | yes | Document file to extract tables from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Optional recognition mode sent as a request header. Default: `Advanced`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "successful": true,
      "tableResults": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `successful` | boolean | Whether table extraction succeeded. |
| `tableResults` | array<object> | Tables extracted from the document. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/tables` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-document-tables.md) for the provider-specific parameters and requirements.

