# Document AI: Extract Document Field Values Advanced

Extracts field values from a document using advanced Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values-advanced
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values-advanced?connectionId=$CONNECTION_ID&InputFile=string&FieldsToExtract%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string",
  "FieldsToExtract[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/extract-document-field-values-advanced?${params}`, {
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
| `InputFile` | string | yes | Base64-encoded document content to extract fields from. |
| `FieldsToExtract[]` | array<object> | yes | Fields to extract from the document. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Recognition mode sent as the Cloudmersive recognitionMode header. Default: `Advanced`. |
| `MaximumPagesProcessed` | number | no | Maximum number of pages to process. |
| `Preprocessing` | string | no | Optional preprocessing mode. |
| `ResultCrossCheck` | string | no | Optional result cross-check mode. |
| `RotateImageDegrees` | number | no | Optional image rotation in degrees. |

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
| `successful` | boolean | Whether advanced field extraction succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/fields/advanced` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-document-field-values-advanced.md) for the provider-specific parameters and requirements.

