# Document AI: Classify Document Advanced

Classifies a document using advanced Document AI.

```
GET https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document-advanced
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Document AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document-advanced?connectionId=$CONNECTION_ID&InputFile=string&Categories%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "InputFile": "string",
  "Categories[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentAI/latest/actions/classify-document-advanced?${params}`, {
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
| `InputFile` | string | yes | Base64-encoded document content to classify. |
| `Categories[]` | array<object> | yes | Document classification categories to evaluate. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recognitionMode` | string | no | Recognition mode sent as the Cloudmersive recognitionMode header. Default: `Advanced`. |
| `Preprocessing` | string | no | Optional preprocessing mode for document classification. |
| `ResultCrossCheck` | string | no | Optional result cross-check mode. |
| `MaximumPagesProcessed` | number | no | Maximum number of pages to process. |
| `RotateImageDegrees` | number | no | Optional image rotation in degrees before classification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidenceScore": 1,
      "documentCategoryResult": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidenceScore` | number | Classification confidence score. |
| `documentCategoryResult` | string | Best matching document category. |
| `successful` | boolean | Whether advanced classification succeeded. |

## Native endpoint

Through the native Document AI API, this operation is `POST /document-ai/document/extract/classify/advanced` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/classify-document-advanced.md) for the provider-specific parameters and requirements.

