# Document AI: Extract Document Fields and Tables

Extracts fields and tables from a document using Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-fields-and-tables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-fields-and-tables?connectionId=$CONNECTION_ID&InputFile=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-fields-and-tables?${params}`, {
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
| `InputFile` | file | yes | Document file to extract fields and tables from. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Optional recognition mode sent as a request header. Default: `Advanced`. |
| `preprocessing` | string | no | Optional preprocessing level sent as a request header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fieldResults": [
        {}
      ],
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
| `fieldResults` | array<object> | Extracted field results. |
| `successful` | boolean | Whether extraction succeeded. |
| `tableResults` | array<object> | Extracted table results. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/all` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-document-fields-and-tables.md) for the provider-specific parameters and requirements.

