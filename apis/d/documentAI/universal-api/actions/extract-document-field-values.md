# Document AI: Extract Document Field Values

Extracts field values from a document using Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values?connectionId=$CONNECTION_ID&InputFile=string&FieldNames=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string",
  "FieldNames": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values?${params}`, {
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
| `InputFile` | file | yes | Document file to extract named fields from. |
| `FieldNames` | string | yes | Comma-separated field names sent as the Cloudmersive FieldNames header. |

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
      "confidenceScore": 1,
      "fields": [
        {}
      ],
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidenceScore` | number | Overall confidence score. |
| `fields` | array<object> | Extracted field values. |
| `successful` | boolean | Whether field extraction succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/fields` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-document-field-values.md) for the provider-specific parameters and requirements.

